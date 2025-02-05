## `golang:1-bookworm`

```console
$ docker pull golang@sha256:b8756b7cf2229b2c8a7dcf86d1199e98b2e393e429c34260546a30499cf61c5a
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
$ docker pull golang@sha256:e36fd3af78f13fb7fd27a16ec62370968ecbe113c1dd026c188162109b34c1a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303303465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc5a72b2e895c3a721087870c20d04c72aa64e75a56b82e39caae3dc27c5846`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOLANG_VERSION=1.23.6
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOPATH=/go
# Tue, 04 Feb 2025 18:26:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 18:26:14 GMT
COPY /target/ / # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 01:36:22 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b550be6cb62359a0f3a96bc0dc289f8b45d097eaad275887f163c6780b4108`  
		Last Modified: Tue, 04 Feb 2025 04:37:13 GMT  
		Size: 24.1 MB (24058355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35af2a7690f2b43e7237d1fae8e3f2350dfb25f3249e9cf65121866f9c56c772`  
		Last Modified: Tue, 04 Feb 2025 05:19:13 GMT  
		Size: 64.4 MB (64394292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c5b2c7e8c9fe55da2c1b8cc238ba47ce679c78999f75b92ba3c05984e0b64b`  
		Last Modified: Tue, 04 Feb 2025 19:33:06 GMT  
		Size: 92.3 MB (92325118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd968b00abc2f44f5d74b014d2b833a05dd020b5f534f19dca853c409df33466`  
		Last Modified: Tue, 04 Feb 2025 19:32:46 GMT  
		Size: 74.0 MB (74045855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb54fd7982a88fa78ada6fd77866de8386d3829004b0f2eca8e9b9b20e44db8b`  
		Last Modified: Tue, 04 Feb 2025 19:33:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:f24ea5097dccaf8dcda44bfb6fb21f68003f44d02072cb343980749085c6a14f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10306952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf861ee9a055c5420cedffbec75abe4f17708c07b23e04ceea6e4b8f722a6a5`

```dockerfile
```

-	Layers:
	-	`sha256:7277a7bfcd37676d684c3b652d06a59867b429bfbb66fd6a6d5c69c433bab550`  
		Last Modified: Tue, 04 Feb 2025 19:33:04 GMT  
		Size: 10.3 MB (10279306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bab80639a8d3d5e9889f48d0254962093c17c2daf68b313c01ac9b7a698d60a`  
		Last Modified: Tue, 04 Feb 2025 19:33:04 GMT  
		Size: 27.6 KB (27646 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:65bdc6ccec24fe76a539b2db211648de5050011c25945e262ace714a54102a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.2 MB (264162228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0482594f0ec29dd84682823707ada7e953de21c3044ae804c047078455a24f7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOLANG_VERSION=1.23.6
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOPATH=/go
# Tue, 04 Feb 2025 18:26:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 18:26:14 GMT
COPY /target/ / # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bf65c309bba1c843ac26792f2d942bca2d7bfcc7024ba331cdfbb762d7573e8a`  
		Last Modified: Tue, 04 Feb 2025 01:37:07 GMT  
		Size: 44.2 MB (44184052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dba4073c18c1d2882f0eb9a2b0d9bf057770ac1b8829e3e149a095273df800`  
		Last Modified: Tue, 04 Feb 2025 10:41:49 GMT  
		Size: 22.0 MB (21960085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66806698bb37ab9f15c9072a66ade0dcacacec8794e48afd7fdc2e801ccb928a`  
		Last Modified: Tue, 04 Feb 2025 16:20:53 GMT  
		Size: 59.6 MB (59639147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495fc29bc2ed109c3df977c363822d9e02d7dfbd66c67a0ed2643726ec489e4b`  
		Last Modified: Wed, 05 Feb 2025 00:35:10 GMT  
		Size: 66.2 MB (66183449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889cc3ffbe9c2ad3a046f41cd3f0630b058873fcf3511968c20cf71cc826b741`  
		Last Modified: Wed, 05 Feb 2025 00:37:25 GMT  
		Size: 72.2 MB (72195337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a27a723bb944380defbaa4c09d07546c0faae12895ac3eb35573bd6ea72886a`  
		Last Modified: Wed, 05 Feb 2025 00:37:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:1bd021868d5b87aa27dc0b89c9612b9009afaad352a1de03fd52a48ee2b4a18e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10115444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31ffaf2d76e9822155b9096384029b7ba80f23c9fd4af8dc4ce2c38efe90d92`

```dockerfile
```

-	Layers:
	-	`sha256:1f6336e495d245962a95e7cb83bd1e58e870d38c567df6ea8a332e01b8bb93f0`  
		Last Modified: Wed, 05 Feb 2025 00:37:23 GMT  
		Size: 10.1 MB (10087664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ee7011683976912f109c63a9bb9e775d37b0ee798c54a0ad13a8b114e2fe642`  
		Last Modified: Wed, 05 Feb 2025 00:37:22 GMT  
		Size: 27.8 KB (27780 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:4db094ea5928a820995f0795c801f14f836654aa9b8b3715208e6d2acbff5094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.3 MB (293314283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f8ac52899d3128b0fcee6dcc79d8cfc9d7bfcb7b54006d64cb92a2eec655dca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOLANG_VERSION=1.23.6
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOPATH=/go
# Tue, 04 Feb 2025 18:26:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 18:26:14 GMT
COPY /target/ / # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193c44006e77abbadfdd7be72b4ab6d7a5c08640ef575970f722b798ee7800ac`  
		Last Modified: Tue, 04 Feb 2025 09:00:06 GMT  
		Size: 23.6 MB (23598428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d3572a68af0b860060b7ea84adfa8406fa20cfd1337c947dfb661aa965eee7`  
		Last Modified: Tue, 04 Feb 2025 19:01:50 GMT  
		Size: 64.4 MB (64357505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac3f7121b9240f61d416dba8be2c96da4ffe9fe1f25831725071946bb7fc54f`  
		Last Modified: Wed, 05 Feb 2025 02:01:52 GMT  
		Size: 86.4 MB (86378491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7476bebdd25fd50c45ff4efca639719b1581613f3017c85f08e38a2d5a441f`  
		Last Modified: Wed, 05 Feb 2025 02:03:26 GMT  
		Size: 70.7 MB (70673148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aadbcf961e9a7aae44f7f000f4c328274edb245b86a4c3dfac539c3376f1f77`  
		Last Modified: Wed, 05 Feb 2025 02:03:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:1acb403cbd1fc922614086b863727dd4dcdde18e0e98246a0ba6c4f4e085a3db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10335029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11cf4f0a024607434920a0802ea7992741e6b5728619345a3a512f2aeadbc85a`

```dockerfile
```

-	Layers:
	-	`sha256:71fd8fee4b24fc59876f7b15e256c61e5e282abc9aefe4bd924312e4804e4ce7`  
		Last Modified: Wed, 05 Feb 2025 02:03:24 GMT  
		Size: 10.3 MB (10307201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e65af15bdc2bf0ec999f47074465fcac03eb795b076c224762f61787a37e48f`  
		Last Modified: Wed, 05 Feb 2025 02:03:24 GMT  
		Size: 27.8 KB (27828 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; 386

```console
$ docker pull golang@sha256:951245bb3d9b2a87c54e7117ef020b1100f1ac0597dba9a4b0355130487cc454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302244474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f83e90fb5283a0ffbf679885d215dbc556ce17bc60f2eff64c960872b4d2282`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOLANG_VERSION=1.23.6
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOPATH=/go
# Tue, 04 Feb 2025 18:26:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 18:26:14 GMT
COPY /target/ / # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d6abb78404200438eb560450e089a4e7707a23d5ec913df260500d902666670a`  
		Last Modified: Tue, 04 Feb 2025 01:36:35 GMT  
		Size: 49.5 MB (49457456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7d7e5b6420845d0479145c8a18a31030093be0de73e11194d97fee1ac58ef5`  
		Last Modified: Tue, 04 Feb 2025 04:23:48 GMT  
		Size: 24.9 MB (24899338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43394bbbaab482132a05c8eb702c9ebbbf5ecccd558ce05fdf40c651b7fbfa10`  
		Last Modified: Tue, 04 Feb 2025 05:15:47 GMT  
		Size: 66.2 MB (66236925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df6eec8bf8ad44f1ce4bd3e948a0c18caf67917e27c54afa53f20213b220a73`  
		Last Modified: Tue, 04 Feb 2025 19:33:05 GMT  
		Size: 89.7 MB (89730783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b77728945927969d0c8ded023b60910b4b7d2a79c658271ebe4948de9a6d578`  
		Last Modified: Tue, 04 Feb 2025 19:32:35 GMT  
		Size: 71.9 MB (71919814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63194ff9e8aa55634465ae28e0ae83cb0c1654323963832e322a84b042862498`  
		Last Modified: Tue, 04 Feb 2025 19:33:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:22f0a27b393fc3818194ce56ea557e49001c89c60fa60e9e98f3366d4361c351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10286950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060a492ada73a9ef1766ee1085e1b2c5646abbba7935701818ee5b8287b2e674`

```dockerfile
```

-	Layers:
	-	`sha256:4ccab193b1798216bd395e48c1812ab89310d243d5642580c021c77d30262b5a`  
		Last Modified: Tue, 04 Feb 2025 19:33:03 GMT  
		Size: 10.3 MB (10259361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab442c8e5a46931b662b1d737d86b107f9476002f556e5e5c8772dedb92572d0`  
		Last Modified: Tue, 04 Feb 2025 19:33:02 GMT  
		Size: 27.6 KB (27589 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:2510908c0ef14566cedc91a45049449ca497c98a59c7e911bbe923a448258c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.9 MB (273919188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0997c462fac600ee41ff111bcfd4efd0ca6efceb99047a9b19fe6e0b5efa0a3a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOLANG_VERSION=1.23.5
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOTOOLCHAIN=local
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOPATH=/go
# Thu, 16 Jan 2025 21:14:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Jan 2025 21:14:07 GMT
COPY /target/ / # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:12e528bcd428b4b8475a045cfdce724675384eedf195bad13ce8015853db632c`  
		Last Modified: Tue, 14 Jan 2025 01:34:57 GMT  
		Size: 48.8 MB (48758103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dede5b838e92cbab015cc8e31645fbe220ba02a56693e3a7a144e0a5428690`  
		Last Modified: Tue, 14 Jan 2025 18:10:17 GMT  
		Size: 23.7 MB (23652164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be7513211e793708951d273ea21ae802b4bdb4109f4b12ca6122e317851db90`  
		Last Modified: Wed, 15 Jan 2025 02:00:51 GMT  
		Size: 63.3 MB (63296729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf120b14fcd2ab38276bd2c721d84ee4295f692d8b46582b8e8b0925a7122fb`  
		Last Modified: Wed, 15 Jan 2025 18:19:55 GMT  
		Size: 69.9 MB (69897363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0329b996be8086919b48075cb5b2356eac5df82347c83695cf847d8135c3b448`  
		Last Modified: Thu, 16 Jan 2025 22:12:41 GMT  
		Size: 68.3 MB (68314671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d36b90d51d82637c2502374b7b4d7606ba64d83e8b3154589db62aafe4fc7ca`  
		Last Modified: Thu, 16 Jan 2025 22:12:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:a34e4a0f040aa1ac988b3288f30f335052a52505155940044efc0abe224900fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a84b8863e209d789196f052c463569e5ad70a5553663a6b3230e2b98ad8dfdc`

```dockerfile
```

-	Layers:
	-	`sha256:2aef82940731124e68a839c7c4a2400a7176679c88e44be8b3d422c6c4492d7c`  
		Last Modified: Thu, 16 Jan 2025 22:12:34 GMT  
		Size: 27.5 KB (27538 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:1ce57761ed49ea0a7647d2478683eecc6dbcd824583f17a0c00555efddb57853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.0 MB (309031058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12fa4b549eee2a962bd25b2c423f6cf96a946dd0e8017d85b2c19b00a9d3f38a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOLANG_VERSION=1.23.6
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOPATH=/go
# Tue, 04 Feb 2025 18:26:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 18:26:14 GMT
COPY /target/ / # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d32dc8295067a6f744a1fca9cfffe021a324e651f2834ad7b587e0380c3f2981`  
		Last Modified: Tue, 04 Feb 2025 01:37:34 GMT  
		Size: 52.3 MB (52312857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f161b1ac6fcd1e84495441a30458604c921f0c00816d0cd0926964e56d9717`  
		Last Modified: Tue, 04 Feb 2025 07:24:32 GMT  
		Size: 25.7 MB (25717668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7451c2aa1d936ee2bec4ea4db323da11f1dc2694095c250c16b70763100f29cf`  
		Last Modified: Tue, 04 Feb 2025 15:46:48 GMT  
		Size: 69.8 MB (69842739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3625fd5449702b0d8fa61c0c059218a9f27e0ee625784b4c5b5b74adb48030d7`  
		Last Modified: Tue, 04 Feb 2025 22:33:20 GMT  
		Size: 90.3 MB (90319530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76bc8515280eafb56fff5db8a8a3f9b1389a9563753c21ecf558291e30e86e2a`  
		Last Modified: Tue, 04 Feb 2025 22:34:44 GMT  
		Size: 70.8 MB (70838106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeaafcdf9205d499310e35a91d4d1cda4bac603424d6c5b5662ea3da9160d5fe`  
		Last Modified: Tue, 04 Feb 2025 22:34:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:25761781e08f72d41c66bdab83e1f4a4e54dd7da1de472148affc3ea40ce8fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10279743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8e46ac0e6ecab02cce5e3f611aec11746b664bc227c6fe65ec6d98a1ac8311`

```dockerfile
```

-	Layers:
	-	`sha256:08e7b7482ab071f6d3537173c69286e8830c8996b439e53a44c68596d8444e9b`  
		Last Modified: Tue, 04 Feb 2025 22:34:42 GMT  
		Size: 10.3 MB (10252025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40c59cf3967ddee523473e122588841717b22790aaa82ca9b96d33de0ba7cc77`  
		Last Modified: Tue, 04 Feb 2025 22:34:41 GMT  
		Size: 27.7 KB (27718 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:f814a5633ac3ee79017a5362f9c6445453e397f0cdad1778895694141e2e4927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276550066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9fe7fdc7e00b43bdb35771b023363cdf0c248a5370ff1a647f7a6480307ff8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOLANG_VERSION=1.23.5
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOTOOLCHAIN=local
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOPATH=/go
# Thu, 16 Jan 2025 21:14:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Jan 2025 21:14:07 GMT
COPY /target/ / # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:21aa15808dc85b52fca40d40118565ddcd1b7ca60220d34328c38ccbc43c6ec1`  
		Last Modified: Tue, 14 Jan 2025 01:34:07 GMT  
		Size: 47.1 MB (47131782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba976031c967b4215afb8ec45dd7db082bb0d532971c83a1e9acaaa24c91981`  
		Last Modified: Tue, 14 Jan 2025 04:59:37 GMT  
		Size: 24.1 MB (24057754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41403619947915f481f99b2b28eecf7aa168ff32ff64e044d73a504ac7472026`  
		Last Modified: Tue, 14 Jan 2025 09:09:48 GMT  
		Size: 63.5 MB (63498283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01efc275df65925eac4d0751075d4662dbb1f25949df2abd249bd7ca26b4c480`  
		Last Modified: Tue, 14 Jan 2025 11:21:34 GMT  
		Size: 68.9 MB (68907405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b567a3d856120b002d262f7c532f30adaa977477b055fda3e7047c19dfbefeb`  
		Last Modified: Thu, 16 Jan 2025 22:11:06 GMT  
		Size: 73.0 MB (72954684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7995ea99ee4b70e2dab7e67d9e8182759e689f59470e006e193c95fe71aee7`  
		Last Modified: Thu, 16 Jan 2025 22:11:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:85142eb50d5d4eb61d351cb1147500e17eb2219659ee7ccba22e534f546319c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10142932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e134df1069af3a34472c1ab2b84f1abf5234cb72b38e6766e34c23ec04f5319`

```dockerfile
```

-	Layers:
	-	`sha256:2396b3cce4344cef8e453b4f4283257fd580c8024a352d4a04236ddf0bfec6f2`  
		Last Modified: Thu, 16 Jan 2025 22:11:05 GMT  
		Size: 10.1 MB (10115286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db303f03ab327280f4ca15ca8d933eac5d0b264b4a802741e164b58fd7230ad0`  
		Last Modified: Thu, 16 Jan 2025 22:11:04 GMT  
		Size: 27.6 KB (27646 bytes)  
		MIME: application/vnd.in-toto+json
