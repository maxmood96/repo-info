## `golang:tip-bullseye`

```console
$ docker pull golang@sha256:3b65fe947dddf1bb59dcff38b39661de9f8d24125b023c46fb93c7ebd9ef5139
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
$ docker pull golang@sha256:65a8dfd0c4efe5dd6a909ba5fada8531d94b491e4c0507408f8a488896e9a68c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (336018838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33af62457e5a3bd760cd91ec1970c961a2d36a039534bd9d30cb0a1669f54d6a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 17 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 17 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8d1bfb80edb9306e3de72f4095daeae4c281712482255562f2e236ae85233e7d`  
		Last Modified: Mon, 17 Mar 2025 22:17:19 GMT  
		Size: 53.7 MB (53741275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aae550f4768ad83c7dcc1ef8de6de078a33effa152d846f4604ead4cbb1f414`  
		Last Modified: Mon, 17 Mar 2025 23:13:33 GMT  
		Size: 15.6 MB (15558355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a322d21cc1b9c3e86a0528fd885e7483a3b2497c1448256bf87a4493be665ab0`  
		Last Modified: Tue, 18 Mar 2025 00:18:59 GMT  
		Size: 54.8 MB (54752320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18dbcd717a93ab387826d798288b9edb796e41dac4a8799e9292dcb69ec6411`  
		Last Modified: Tue, 18 Mar 2025 03:20:16 GMT  
		Size: 86.0 MB (86000936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41a83b25ec0e0c49ecd36fb9980281b7ce15ce7da6877f867a2e7766c298175`  
		Last Modified: Mon, 17 Mar 2025 21:13:26 GMT  
		Size: 126.0 MB (125965793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb842ba460383981e7e8e4b1f476f0b6f5b81aa783b7064a9db9c30f7aac26ef`  
		Last Modified: Tue, 18 Mar 2025 03:20:15 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:aae5d82e844903512508235bbfd35e05583aa6827544a554a9db8b7eecb0d9a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10291346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb1ff08a810691c069d44874eb511fef970d1bc28d7efc29ba088c60685f00e`

```dockerfile
```

-	Layers:
	-	`sha256:c9648a91eacb9f8fa48cf8f003f7535ad243dde115f7f586ca63dcfca4b60b31`  
		Last Modified: Tue, 18 Mar 2025 03:20:15 GMT  
		Size: 10.3 MB (10264285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:992d17ec607350403ed25d222972d572733c3ae0a3df55fa08fcf16c6f0c66f4`  
		Last Modified: Tue, 18 Mar 2025 03:20:15 GMT  
		Size: 27.1 KB (27061 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:d8de68726a53a5f0013ea840481417448324f5d0908732deb382ac1f3cc68915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.5 MB (302507806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb35a21247e988d3a0662cdec8da23d46a2694c62796992686ebb4cb6f63aa5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 10 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 10 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 10 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 10 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b371c05b17ddc4521fa62e27633ef500c9e18d0922c933dc30ad692d163a6adb`  
		Last Modified: Tue, 25 Feb 2025 01:31:01 GMT  
		Size: 49.0 MB (49026733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce7f37fed942ce7eb6947b63b02cebac1a836c49ae19b59c3dfd4d0dafde5e9`  
		Last Modified: Tue, 25 Feb 2025 07:17:13 GMT  
		Size: 14.7 MB (14673973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3908d2a88cdaeb59d430f53cffe54008e1006a05c4aa7a391f2dce9c9b9aff8`  
		Last Modified: Tue, 25 Feb 2025 14:18:51 GMT  
		Size: 50.6 MB (50640099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0260b683984b5458b67512624176ac3f678832da5b7aa4c808cea1226ddb01`  
		Last Modified: Tue, 25 Feb 2025 17:02:06 GMT  
		Size: 64.9 MB (64892946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca61e995b8c13d851dd3e3c6f227fdb4c36ab271e17ec8b18961597fba4895b4`  
		Last Modified: Mon, 10 Mar 2025 21:09:26 GMT  
		Size: 123.3 MB (123273897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc442559597921b1a2758af574fece310ac042b55d384ee9f072e8a3c6a3bb3`  
		Last Modified: Mon, 10 Mar 2025 21:13:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:42f5e8d4639645d921997d3fad86f93f942d5c56edeadd4a5587845e95dba207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10097794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0918384f631fab9bdc83d5c8ff2d2f7fe5d1cc18b0a32d302f6eddadfffed9`

```dockerfile
```

-	Layers:
	-	`sha256:222976252f7a5e70e1386c69b8dd8f614797a866a247fc5f9c8770c605aaf79f`  
		Last Modified: Mon, 10 Mar 2025 21:13:06 GMT  
		Size: 10.1 MB (10070625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:732be7fe493ce4a59a935d71221cde8700d2541dd2463710fbad8200d6dc433e`  
		Last Modified: Mon, 10 Mar 2025 21:13:05 GMT  
		Size: 27.2 KB (27169 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:94cd027c55cd25a3d9ac5338797daec2f539bd8d2ba53f052ecd58dd0db8190c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.9 MB (326860188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb418f9645e0abcce79597a02a86ab3be1bc0515ceb520b9422c341882d4759`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 10 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 10 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 10 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 10 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7e1cabb756c27ddad3e1de86c2aaf2bca04f012bff531cd99d37f98896026ca4`  
		Last Modified: Tue, 25 Feb 2025 01:31:16 GMT  
		Size: 52.2 MB (52248644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7364a649b3acc0e2c47a31825e92a687c9eae217b5c8c062f3efaabe7bec06f7`  
		Last Modified: Tue, 25 Feb 2025 05:42:11 GMT  
		Size: 15.5 MB (15544146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8a227b92685cb13561fe06ec9cfa79231e26157c7e163ab5b9af993e63bd10`  
		Last Modified: Tue, 25 Feb 2025 11:54:42 GMT  
		Size: 54.9 MB (54855421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c63332dc2fc1cf0757c0675d81bf024aa3d2b601d0c397704255d7fd384be6`  
		Last Modified: Tue, 04 Mar 2025 00:42:12 GMT  
		Size: 81.4 MB (81413797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e9a129027ad3875ac19234bac00390ebdd61f752809a25128556ac5b500a6c`  
		Last Modified: Mon, 10 Mar 2025 21:42:38 GMT  
		Size: 122.8 MB (122798022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2bd2a9bd858e83545f424b24dc1447b3e40a4d42d177353a361b3df8a79309`  
		Last Modified: Mon, 10 Mar 2025 21:46:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:e32c30470faa5f2e19a177b1d66b300a7adf548a0ab2758302b690e2d1146550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10293054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb48db15171f15cc835ba88f20e16923c2179f3847b87ce5c71a1411df1aa5de`

```dockerfile
```

-	Layers:
	-	`sha256:f616284bcf23f00af9f13d23cb8ca77128b5dcb36fb6bc47c34fdc7ebc7276c0`  
		Last Modified: Mon, 10 Mar 2025 21:46:27 GMT  
		Size: 10.3 MB (10265857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2aba816888b274f28cf46190ee2e7d2d0de11471ae30e49193623200d67228b`  
		Last Modified: Mon, 10 Mar 2025 21:46:26 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; 386

```console
$ docker pull golang@sha256:52bd0530811f03af639b922a4334f4cdc8a2c8974fa6547cba34ca23c0ece73d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338265884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6461bec62bb89da9b2a520e905be30771ffae52560f587a974aabb9cdbe10e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 17 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 17 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 17 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b2bf052a55a1540734073d8a106c4845ec09ac4ac8cc46a275584d3eef876deb`  
		Last Modified: Mon, 17 Mar 2025 22:17:43 GMT  
		Size: 54.7 MB (54678617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5503af74d5075005e8a2caef8b6b369ec49cf0d7a20dcdd1fe79d68aa4ba6c`  
		Last Modified: Mon, 17 Mar 2025 23:32:34 GMT  
		Size: 16.1 MB (16062045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfffc7337857c58b61734136d663ca328549ab864bf18f3217e50e3fdc25680`  
		Last Modified: Tue, 18 Mar 2025 00:18:53 GMT  
		Size: 56.0 MB (56030008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7ac19cd1eed86b56d622cd8d86dfe17c75b10a46dd0f65dcce176a56b76511`  
		Last Modified: Tue, 18 Mar 2025 03:20:57 GMT  
		Size: 87.4 MB (87426475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a94495553b1c250ac72571d6400e4136caa9f00d345a28d3faea166cf26f298`  
		Last Modified: Mon, 17 Mar 2025 21:14:00 GMT  
		Size: 124.1 MB (124068582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c8a4ee7da0611c4b463108fd35764b2347634ae024e4a51a1322a1f870267d`  
		Last Modified: Tue, 18 Mar 2025 03:20:54 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:53cd8744ea08481ac8b2803a9b012e8264b876c66cd83f6c0b94d2731023ae63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10281104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0033b00d4f2a017ae3c320949d6391c9e670895aaa368f1a0210e43b66b02b4a`

```dockerfile
```

-	Layers:
	-	`sha256:9cd2f64cd1d54d413203e3a6744627e3f53f16bf84fd7bfa172b1a6918c2cea2`  
		Last Modified: Tue, 18 Mar 2025 03:20:55 GMT  
		Size: 10.3 MB (10254076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a8caf72a4dd1f6817f5b703d07440a211c758bcf1e391b6a4f4bb29b1cd7db2`  
		Last Modified: Tue, 18 Mar 2025 03:20:54 GMT  
		Size: 27.0 KB (27028 bytes)  
		MIME: application/vnd.in-toto+json
