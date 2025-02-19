## `golang:tip-bookworm`

```console
$ docker pull golang@sha256:69da007532883c400413d41f0f3cd13b29ab0bcdf44df4b970df7f2f60187e39
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
$ docker pull golang@sha256:e8de6ce942ed29cd522adb8f0d9f38646695922c0df134c39de9fb99b8041cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.8 MB (358797104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e07ad5e15dde573321a914e4843f67f03462404eb18b51db2b0ed39ba667be`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOPATH=/go
# Tue, 18 Feb 2025 12:02:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 12:02:31 GMT
COPY /target/ / # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 04:24:49 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b550be6cb62359a0f3a96bc0dc289f8b45d097eaad275887f163c6780b4108`  
		Last Modified: Tue, 04 Feb 2025 07:11:25 GMT  
		Size: 24.1 MB (24058355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35af2a7690f2b43e7237d1fae8e3f2350dfb25f3249e9cf65121866f9c56c772`  
		Last Modified: Tue, 04 Feb 2025 08:41:29 GMT  
		Size: 64.4 MB (64394292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7583210f7301477d03285218575b3868d5f0bd6f8920039d780e623f285948c`  
		Last Modified: Wed, 19 Feb 2025 00:31:49 GMT  
		Size: 92.3 MB (92332178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7cc5764bfa5625e90d4c9d1c4bb7361ceb8d3451c8f3534f5e3a80e9f8aa6e4`  
		Last Modified: Wed, 19 Feb 2025 03:27:14 GMT  
		Size: 129.5 MB (129532433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98df8947d13e7d75a57c81fd72feb7400d86c45d625bfacbc4198be998e2f2d`  
		Last Modified: Wed, 19 Feb 2025 00:31:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:4f2216a5b9c6215257af7dd9521f83370f89e76b17b57e9067f8097826de80a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10304520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9acfa0237535e5ac5bdf44d630ce982a4e29d4d8974cbcf04c61e2a1b420ef`

```dockerfile
```

-	Layers:
	-	`sha256:33a3f9266855008f8048652187953f00b7339e22211e51af541bab6229e5b1d0`  
		Last Modified: Wed, 19 Feb 2025 03:23:33 GMT  
		Size: 10.3 MB (10276857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:594763b3a74d6e962c442de869992222985f4b6285a4526e0be097167b9d77b5`  
		Last Modified: Wed, 19 Feb 2025 03:23:34 GMT  
		Size: 27.7 KB (27663 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:394d7e54437cece1a352c08b59befb439d8ae5272bbca8319a1704d68f49c66b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.8 MB (314765156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf1053a1c872ccf9c5f7f7d9c5400988eb107afb70db383a93a601999aa25bdc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOPATH=/go
# Tue, 18 Feb 2025 12:02:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 12:02:31 GMT
COPY /target/ / # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bf65c309bba1c843ac26792f2d942bca2d7bfcc7024ba331cdfbb762d7573e8a`  
		Last Modified: Tue, 04 Feb 2025 05:02:17 GMT  
		Size: 44.2 MB (44184052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dba4073c18c1d2882f0eb9a2b0d9bf057770ac1b8829e3e149a095273df800`  
		Last Modified: Tue, 04 Feb 2025 23:37:50 GMT  
		Size: 22.0 MB (21960085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66806698bb37ab9f15c9072a66ade0dcacacec8794e48afd7fdc2e801ccb928a`  
		Last Modified: Wed, 05 Feb 2025 04:00:39 GMT  
		Size: 59.6 MB (59639147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495fc29bc2ed109c3df977c363822d9e02d7dfbd66c67a0ed2643726ec489e4b`  
		Last Modified: Wed, 05 Feb 2025 03:31:27 GMT  
		Size: 66.2 MB (66183449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbce18d551f744b2f9a445aaedbcd8c5e283783570d9da4735469555773098f`  
		Last Modified: Wed, 19 Feb 2025 01:09:47 GMT  
		Size: 122.8 MB (122798265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cf5aff552863580fddfd7ef5e7b9ab49b6150f94a3b895fe29648c37f52889`  
		Last Modified: Wed, 19 Feb 2025 01:09:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:527c7f620d0ce1eee722ce5dc26a531c9955be31a336e7e358a4f9c34b1574d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10112966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71adc065c035c4f31e947058bbf5c5cf31b8f1a7337c6e32c1635dfeeb582738`

```dockerfile
```

-	Layers:
	-	`sha256:44a9748e77da5019f432218e4f96178b8b305148d76dda87cfdea7fa6a4fc9fc`  
		Last Modified: Wed, 19 Feb 2025 03:23:38 GMT  
		Size: 10.1 MB (10085179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:963de86a91843aa29017c101ae861da41e5557284fe6fa7291aba60a1090ca9a`  
		Last Modified: Wed, 19 Feb 2025 03:23:39 GMT  
		Size: 27.8 KB (27787 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:3f6695ee38fdbc32fe6c69d4dfc3910f140733249dc92528c1415198b2aa2eef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.0 MB (344994427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:451a28948b6135fc0e3046f65b2ec35ffdd81a3a6ccb637e03f6db9d23ab8fdf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOPATH=/go
# Tue, 18 Feb 2025 12:02:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 12:02:31 GMT
COPY /target/ / # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 04:37:12 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193c44006e77abbadfdd7be72b4ab6d7a5c08640ef575970f722b798ee7800ac`  
		Last Modified: Wed, 05 Feb 2025 00:14:09 GMT  
		Size: 23.6 MB (23598428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d3572a68af0b860060b7ea84adfa8406fa20cfd1337c947dfb661aa965eee7`  
		Last Modified: Wed, 05 Feb 2025 02:21:14 GMT  
		Size: 64.4 MB (64357505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac3f7121b9240f61d416dba8be2c96da4ffe9fe1f25831725071946bb7fc54f`  
		Last Modified: Wed, 05 Feb 2025 02:18:50 GMT  
		Size: 86.4 MB (86378491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5298385c49d911d309658b69d6f0a6876dfdb4d5bed9f2c1fff825ca2fb2fcdb`  
		Last Modified: Wed, 19 Feb 2025 00:41:18 GMT  
		Size: 122.4 MB (122353292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee5d6bcd8f95af292e797d054b89e50e7a3b1593c1bc320434bec8406eb0fe9`  
		Last Modified: Wed, 19 Feb 2025 00:40:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:1b5be109c0a818b11c57f97ed0097d79fd11e0566ecfe1561873481ff976ae0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b3777cbeba7c68c651861e0102ff72b538e35ef91bb70ab1d8082851bc4fbb`

```dockerfile
```

-	Layers:
	-	`sha256:25eabd50a4f1069c43be62a22855aae2ed1f3733b33b5b7686db6a7428680763`  
		Last Modified: Wed, 19 Feb 2025 03:23:43 GMT  
		Size: 10.3 MB (10304704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9c6ebd66439f01e07eab15fa8eea02178f6cfc1c9a8971f11fdea2c8d1d24fe`  
		Last Modified: Wed, 19 Feb 2025 03:23:43 GMT  
		Size: 27.8 KB (27823 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; 386

```console
$ docker pull golang@sha256:b77c683003a1cdb2809194decc8884885f99ea9d5e5c5dd0d180085ca4cda788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.5 MB (356505157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:006ddf9f8d75e086bcd366250de2172e4a1b7149096fad10982ae73bed0a6ef6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOPATH=/go
# Tue, 18 Feb 2025 12:02:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 12:02:31 GMT
COPY /target/ / # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d6abb78404200438eb560450e089a4e7707a23d5ec913df260500d902666670a`  
		Last Modified: Tue, 04 Feb 2025 06:02:17 GMT  
		Size: 49.5 MB (49457456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7d7e5b6420845d0479145c8a18a31030093be0de73e11194d97fee1ac58ef5`  
		Last Modified: Tue, 04 Feb 2025 10:18:57 GMT  
		Size: 24.9 MB (24899338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43394bbbaab482132a05c8eb702c9ebbbf5ecccd558ce05fdf40c651b7fbfa10`  
		Last Modified: Tue, 04 Feb 2025 09:42:09 GMT  
		Size: 66.2 MB (66236925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da04c273db0cde5beaf719f21657592c3151c6d39aff291f2efd69e19b0a8fe`  
		Last Modified: Wed, 19 Feb 2025 00:32:11 GMT  
		Size: 89.7 MB (89744340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c865367c21802db35d933085cc324482ddcbb8bd28bfbcd89b6ea5d6a248d00d`  
		Last Modified: Wed, 19 Feb 2025 00:32:09 GMT  
		Size: 126.2 MB (126166939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d8e261dd0e83534fd0600a6e5d2777a17cf3b9964027f7c57aff6ee4eeb658`  
		Last Modified: Wed, 19 Feb 2025 00:32:02 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:2b6a544fe300bcd82442df1e40d80003f1a3fcc2b77cef2911ac3f95619e4a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10284548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:132bfea799b88e66cc332902d00ac0dd6df8eda30dbb4f3be63f1a3057fd6eac`

```dockerfile
```

-	Layers:
	-	`sha256:c4e9c28d06abbff7d0b1aa763945e80544b5fec2da28ce5d0ee567aea92dc9aa`  
		Last Modified: Wed, 19 Feb 2025 03:23:47 GMT  
		Size: 10.3 MB (10256928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:633005c696ea1e206c7bc930f24ea5c94c328b4297f9c6c800f4491d9c304123`  
		Last Modified: Wed, 19 Feb 2025 03:23:47 GMT  
		Size: 27.6 KB (27620 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:dfaf7ed1e2aa4731da5c47cce9d2dc0bcee2794def304acd371fadc2271aaff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.1 MB (325063484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb757e436050d34b5bb822bbff27d8c745cc100c29e157677b49e8e25edc8d34`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOPATH=/go
# Tue, 18 Feb 2025 12:02:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 12:02:31 GMT
COPY /target/ / # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:467081b053e1cbae3c04ca1529cea6d968f9b38249f5cdd15b07f60be084dd00`  
		Last Modified: Tue, 04 Feb 2025 06:00:54 GMT  
		Size: 48.8 MB (48757800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7faf65582b7e0fbb4eea14df7537078630b3bff0936e1fc964a494519326b5b`  
		Last Modified: Wed, 05 Feb 2025 04:01:51 GMT  
		Size: 23.7 MB (23652224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12393adfa37a97fbcfa8d29955e04828c6bd657b4d83082cf837413910af04a1`  
		Last Modified: Wed, 05 Feb 2025 10:04:59 GMT  
		Size: 63.3 MB (63306362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad120905a0f60eab99f4ab665554fe053a33e4959cc10d9453a31e032d47eea`  
		Last Modified: Wed, 05 Feb 2025 09:31:55 GMT  
		Size: 69.9 MB (69897902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f533a5cfcdbf5b94d7211b45e3a842aae1ef6cb651e9261297a7e03d20fc67`  
		Last Modified: Wed, 19 Feb 2025 02:04:38 GMT  
		Size: 119.4 MB (119449039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0e5581ffc04ca59e19623c7041ba7f56248add5c485d4ddc96f8f6e9e867a3`  
		Last Modified: Wed, 19 Feb 2025 02:04:31 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:f3cf89838df75575c6e3cbcfc5e64748d834928889e65aadaf1101f8329ccad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd654cf6003af21e1dc69fea049348f305ba8d57b0a2a9e2212ec01d72befc8`

```dockerfile
```

-	Layers:
	-	`sha256:c94c4264d82cb9ab71d69a3374a663724b0ab93fbc555ba4c2f0488433087de1`  
		Last Modified: Wed, 19 Feb 2025 03:23:51 GMT  
		Size: 27.5 KB (27535 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:fb0289204b1c1059d7f276efe0badaaf35dc9971f70e7f5a545c3b462e636150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.9 MB (362885950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a60dc3015649a45eafe63615c9ceb4ceeeaae179e9eddf7a5d1e238d442868b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOPATH=/go
# Tue, 18 Feb 2025 12:02:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 12:02:31 GMT
COPY /target/ / # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d32dc8295067a6f744a1fca9cfffe021a324e651f2834ad7b587e0380c3f2981`  
		Last Modified: Tue, 04 Feb 2025 06:02:17 GMT  
		Size: 52.3 MB (52312857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f161b1ac6fcd1e84495441a30458604c921f0c00816d0cd0926964e56d9717`  
		Last Modified: Wed, 05 Feb 2025 00:47:58 GMT  
		Size: 25.7 MB (25717668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7451c2aa1d936ee2bec4ea4db323da11f1dc2694095c250c16b70763100f29cf`  
		Last Modified: Tue, 04 Feb 2025 18:00:23 GMT  
		Size: 69.8 MB (69842739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3625fd5449702b0d8fa61c0c059218a9f27e0ee625784b4c5b5b74adb48030d7`  
		Last Modified: Wed, 05 Feb 2025 00:31:34 GMT  
		Size: 90.3 MB (90319530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c08a2f45c0cbec2efd7e342b73e4171953b8c39e916958809f4e692e3c7803`  
		Last Modified: Wed, 19 Feb 2025 00:37:08 GMT  
		Size: 124.7 MB (124692997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e11520055b079962e03ec82fdd17f7a6d2219d6ec886ddabe549aaf1b6f545`  
		Last Modified: Wed, 19 Feb 2025 00:36:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:6b924b362d57264d4c423c20472d6f84375d676ef73b6891c56ed76abbdd9930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10277277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93f3c6c4b684de59f7df8a36e04bdc65e99d6a8f79eafa84c0c51e4c2f7dfadc`

```dockerfile
```

-	Layers:
	-	`sha256:ff5f7e76dceaf5fe208031d5e72d3df5b192594b06aab448d1ad9c2629e69c32`  
		Last Modified: Wed, 19 Feb 2025 03:23:53 GMT  
		Size: 10.2 MB (10249556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4705c0525279fa7df527960ad73e9679dda705bc095d3700a3bbc9cec5092d6d`  
		Last Modified: Wed, 19 Feb 2025 03:23:53 GMT  
		Size: 27.7 KB (27721 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:6899fe93defb1523ff12100c11b7a3f276572398356466d92c8d6ba6a467790e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.7 MB (330693368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2049633a902471d08ef332c6a97b45a7953a4b5369c207131e7f908474c0b66d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOPATH=/go
# Tue, 18 Feb 2025 12:02:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 12:02:31 GMT
COPY /target/ / # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:92bc3bb38690fde96c4bb788f15f365b04d4cb8ab9368675dc9294bc24a9c7b6`  
		Last Modified: Tue, 04 Feb 2025 05:09:29 GMT  
		Size: 47.1 MB (47131492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe7257ceffda4bd6219bda9d63efd9f5fc932de95d2f5db69f3d95df88e73b0`  
		Last Modified: Wed, 05 Feb 2025 01:13:32 GMT  
		Size: 24.1 MB (24057578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800fd1d6411dfa44ccdbe5db47bb7e970909c1a08d63328dfd165607beb67e7c`  
		Last Modified: Wed, 05 Feb 2025 00:15:03 GMT  
		Size: 63.5 MB (63499455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622f31351dd9f8a683608361b61d9b52cab45259b4b66a1cbdd57f5fb617cfcc`  
		Last Modified: Wed, 05 Feb 2025 07:02:31 GMT  
		Size: 68.9 MB (68907533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8311c8f145699dc7db93b7bdc96735f262ad8c55b79caa71a6a51467909f939e`  
		Last Modified: Wed, 19 Feb 2025 00:48:55 GMT  
		Size: 127.1 MB (127097152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b758e4897fd6b6483b617b932abb0e21d0b1c650441464f17a77a20093c2c20`  
		Last Modified: Wed, 19 Feb 2025 00:48:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:06bc9269c7031b0437dec9740ee4fd01658332fdcf6c0a505cd25ecb842d5e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10140500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdf6cee13b430f35222a118b1fdb19e25329c8eb67a33790031867e89b3fa7a`

```dockerfile
```

-	Layers:
	-	`sha256:0271842d6b6deb393dfe07a463aab5923441c2ace3cf90a91b68e8e94d9553b9`  
		Last Modified: Wed, 19 Feb 2025 03:23:57 GMT  
		Size: 10.1 MB (10112837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:041421c18ce77a785ebe646249b734db3e132ebdc4ede999cdacec8990c9202f`  
		Last Modified: Wed, 19 Feb 2025 03:23:58 GMT  
		Size: 27.7 KB (27663 bytes)  
		MIME: application/vnd.in-toto+json
