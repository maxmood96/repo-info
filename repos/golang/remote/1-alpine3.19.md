## `golang:1-alpine3.19`

```console
$ docker pull golang@sha256:b0aab3c1c38ec4b054317b2721c6fff3e55357506dd69942c83ab9447403dec7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:1-alpine3.19` - linux; amd64

```console
$ docker pull golang@sha256:52bf73b9a2e9b7ec3b3a0b95f6b25e62c7644ccdbe7fd346254967e1d55876c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77760205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9daca17e0f494c9a255650a647b7ebbe9cb69979d76a94bbe505983c13c94d4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 19:01:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e55d31176cfa776019692da65570fb7f9f9d7ecb8bcdb97ef66b332a41e65fa`  
		Last Modified: Tue, 03 Dec 2024 22:28:51 GMT  
		Size: 292.9 KB (292871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f05ace1117d62b655e04f6f73c83617e3e0febc38681dbedf58f477dd0658c`  
		Last Modified: Tue, 03 Dec 2024 22:28:52 GMT  
		Size: 74.0 MB (74047449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f931ef26d2833f529085c8141e621cf72a1277f6524c25ae5550a255ee4c5b01`  
		Last Modified: Tue, 03 Dec 2024 22:28:50 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:0c294a515a0a9a6abd2c4ec0a2fbd804ea75abb450a5d9ab09fc667787fc20e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.9 KB (237893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85f24616dd7ec6541a49d6e0e4e6dcd141c6363f2bb6d28e9a82782f94b4fcb`

```dockerfile
```

-	Layers:
	-	`sha256:e11a7043277fb0fea1e666e53a64c88719cecc94ef6832af4d6b58b76a7248fe`  
		Last Modified: Tue, 03 Dec 2024 22:28:51 GMT  
		Size: 213.0 KB (213043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07f02da32001038488325b6717bba19b817ad534a524c2e863f1a5dc9208fadb`  
		Last Modified: Tue, 03 Dec 2024 22:28:50 GMT  
		Size: 24.9 KB (24850 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.19` - linux; arm variant v6

```console
$ docker pull golang@sha256:0cb6f3aec18d1f7c8fad7c10e3d3bfad5ad9a74a53ed5911c196111b05858893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75669427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c37cea91d478d1b6bf55b300d174c2efedf6b0c5ffba731895fa446c10d58a1a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 19:01:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1962dd3845094270fb16c55729f52e68e09c9fdecbe06ccfa89e981fa679172d`  
		Last Modified: Mon, 09 Sep 2024 07:03:19 GMT  
		Size: 3.2 MB (3176432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7534d0f4f08266b9bfa5441e5b22e4fae47a176f5f809f36c32e131dbeb15a38`  
		Last Modified: Tue, 12 Nov 2024 06:37:21 GMT  
		Size: 294.3 KB (294297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569843b3031b27806b4332ef906025ac81fe5ab3623a61a6d2306598bfd512bf`  
		Last Modified: Tue, 03 Dec 2024 22:28:55 GMT  
		Size: 72.2 MB (72198540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79f486e55918142403398d3dca3d68c774e5b754d20827b815767bdb361e5e5`  
		Last Modified: Tue, 03 Dec 2024 22:29:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:f2476c6b0e2850d3022f50d1881eebe503cd9a5c0af1003b8b4000928aa89a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 KB (24736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1286c2dfca57d19a2fe8e6f841396c25739ddca7e0aa87b92f81524cfa07883c`

```dockerfile
```

-	Layers:
	-	`sha256:10e7dfaf34d2de78dd44361755d86bb155221ae75eb7cf23d7acad78e25e07a7`  
		Last Modified: Tue, 03 Dec 2024 22:29:27 GMT  
		Size: 24.7 KB (24736 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.19` - linux; arm variant v7

```console
$ docker pull golang@sha256:91d5737bc2761c51ff7fff5842b0773d5ab7d5b8b067bb73ddd56350721e6402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75405095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a00217dddd95a5b8d4e95fa1f2a3dc5aea2de1852791a363e1879dc234efd2af`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 07 Nov 2024 00:26:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOLANG_VERSION=1.23.3
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOPATH=/go
# Thu, 07 Nov 2024 00:26:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Nov 2024 00:26:15 GMT
COPY /target/ / # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:02dfd5e2e7e47e8d8f9020a0d7f4d8240d6646afc6a52b168c0899bc0c3d06a3`  
		Last Modified: Mon, 09 Sep 2024 07:03:23 GMT  
		Size: 2.9 MB (2927731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de63640f0d863540d835bbc84ebfaa389f02b4a9cf1120c771fbb6cc9cc5d409`  
		Last Modified: Tue, 12 Nov 2024 17:07:41 GMT  
		Size: 293.1 KB (293121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e990400f8c0342109351b2ea2dff891387190e755f29d02b0f474578fc3d222`  
		Last Modified: Thu, 07 Nov 2024 02:59:45 GMT  
		Size: 72.2 MB (72184086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981d5ab751efe1190f103dfbe037ada4825376a669142b24d8e2f9bc223e60c8`  
		Last Modified: Tue, 12 Nov 2024 17:07:40 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:1043c5c5cc00365ad1523a542b4de1d6906d2dfc5fd9bfb17298c1584fcd5cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.0 KB (237995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d232050cec3b407307f9b733bfc55160a62e411e1dab61beaf30610057d4a39`

```dockerfile
```

-	Layers:
	-	`sha256:941f84fb1cc5d829d1dcf9ca2210cab3bcd712eafe2e725bc309922c73d999ea`  
		Last Modified: Tue, 12 Nov 2024 17:07:41 GMT  
		Size: 213.0 KB (213043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f846cfb5f2fcd70293df575d8deab2c20f2a621b1691874fb2341ff14ba0d33`  
		Last Modified: Tue, 12 Nov 2024 17:07:40 GMT  
		Size: 25.0 KB (24952 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:8d9809daa0d4e406ae0f67d37449b4861cc4baaf68a0ff4b78d2662f9553e914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74324384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb800fd9eaeaa8137457196174518061cf2a60a717b2de4b3ef041f8f9977272`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 07 Nov 2024 00:26:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOLANG_VERSION=1.23.3
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOPATH=/go
# Thu, 07 Nov 2024 00:26:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Nov 2024 00:26:15 GMT
COPY /target/ / # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e31033fd2dbfbcd98437ec0970e2b342f3504008b432c8e456ff92f51b5551`  
		Last Modified: Tue, 12 Nov 2024 12:00:45 GMT  
		Size: 296.0 KB (296033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323003b0d8ad8001283c9881b96c87e9fa38fb378aa4de93c4defd3899f30d2a`  
		Last Modified: Thu, 07 Nov 2024 02:59:17 GMT  
		Size: 70.7 MB (70668948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc2dad70bd58b7c7584c1aade3e50ece5a1db5c0acb1a016064473beed7d878`  
		Last Modified: Tue, 12 Nov 2024 12:00:44 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:82639c2a8de579c649ea587cd4370f2d66136f1fce853ff8343158c563f6cf44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.1 KB (238083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c46daac3be86b30d9ba50dd8e8b69f85d94b194457cd440cb54cc8810d18ea35`

```dockerfile
```

-	Layers:
	-	`sha256:902b4b89b755e1a067e48ddd64c178a31ab9943291b8eabd1e2da0009a82a8d5`  
		Last Modified: Tue, 12 Nov 2024 12:00:44 GMT  
		Size: 213.1 KB (213099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6aa7b037ea7b4ea437017dfa7184b58ae3469702ef21e7c4bf722d0776c9145`  
		Last Modified: Tue, 12 Nov 2024 12:00:44 GMT  
		Size: 25.0 KB (24984 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.19` - linux; 386

```console
$ docker pull golang@sha256:16d5d8b7b5d03ed61eaf98ca4817aa55f328ecba42d3b27c640191ed6091ffa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75460465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d76743b3ed42cb02a79f64b20b95677ac59b1efb569d3aaf32e0fd133eab0426`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 19:01:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ab80d4d2b0222e03eca115215a16260e1a5f86f8b55e9b677e9d5c30b909a6af`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.3 MB (3253666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e6d69efe0d93bd69b0df297419f3ae10ebae0bc56d08050f6fef467c3631b6`  
		Last Modified: Tue, 03 Dec 2024 22:28:47 GMT  
		Size: 293.5 KB (293520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253ee978a239d9a54a2ed89c291f3c5c0ee5f67c1dc8c9ff24b239116398d826`  
		Last Modified: Tue, 03 Dec 2024 22:28:50 GMT  
		Size: 71.9 MB (71913121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8236ecab14218b9227e379280a12ac50468af0def587c1114d36077a482602da`  
		Last Modified: Tue, 03 Dec 2024 22:28:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:70fef090bcda6d2a974cf05a253fe8f71ccb2a1a057ea6c54b9fc46fc0544734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.8 KB (237796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a061cee7ba30e5b79630f69b0e88fa622525be722b9270c7a7fff390ed5a2c85`

```dockerfile
```

-	Layers:
	-	`sha256:c52bbc748b643e18d8f6bf4fc1ff842243d1edfdceaec6aa1d43814df49bad45`  
		Last Modified: Tue, 03 Dec 2024 22:28:47 GMT  
		Size: 213.0 KB (212982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04fadc29fe5429cd5c906074cfc0499e103680cebef53ba2e4fee55bb2ed9fe8`  
		Last Modified: Tue, 03 Dec 2024 22:28:47 GMT  
		Size: 24.8 KB (24814 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.19` - linux; ppc64le

```console
$ docker pull golang@sha256:29ac2ad2eae2be12470400182bcf89d345662ed0f0cf7ae06a49e97e53daa1c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74489587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6668a80fcfb493f997e16a68bd7cb9268c5f3d3f247d8df25471f850346462`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 07 Nov 2024 00:26:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOLANG_VERSION=1.23.3
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOPATH=/go
# Thu, 07 Nov 2024 00:26:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Nov 2024 00:26:15 GMT
COPY /target/ / # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c3045cb4f0dd3320c62c35c3443bc350e64a45c48666004b29e9912a645e7b35`  
		Last Modified: Tue, 12 Nov 2024 00:55:44 GMT  
		Size: 3.4 MB (3364499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b508a3b90d326eb5da57c0221cd72f27d1975d404bbcdb269dba626e586bf2a`  
		Last Modified: Tue, 12 Nov 2024 08:59:50 GMT  
		Size: 296.5 KB (296452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d45dcd888e3183671630e662953341e3111584ee0e6ca4f0d40e50580ea2de`  
		Last Modified: Thu, 07 Nov 2024 03:00:09 GMT  
		Size: 70.8 MB (70828478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13532e25d9fdcb0d09e57d0c378df022c3ad68d5028f6154190a6f7fe25e9a8e`  
		Last Modified: Tue, 12 Nov 2024 08:59:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:dfb809b2ab01942081cc441288e9f3eb5fdedd36c6d43e74fd1b6614ae519e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 KB (236057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91ad5ccb70877aa6907d9dd4ae509a5c66208a1f75d7a4dd75af9e358268b3eb`

```dockerfile
```

-	Layers:
	-	`sha256:205edbaff4465c6da545c53749f44dcdfde08ee32154a8b996abd506b7ff5b04`  
		Last Modified: Tue, 12 Nov 2024 08:59:50 GMT  
		Size: 211.2 KB (211159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28b03fcc086c0d4cf4367cb272c92adc9eec589471a9450e948ee24e9784b054`  
		Last Modified: Tue, 12 Nov 2024 08:59:50 GMT  
		Size: 24.9 KB (24898 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.19` - linux; s390x

```console
$ docker pull golang@sha256:40788ba83fa051f4231a3e9b6262920ff0546a548e7a37b31389efa8740aafec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76517443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2667d5760cdda9f219ee72941a73ca3b13d02847405f890f116c571ca9482cb2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 19:01:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6281353bb84e1beeb4deabf01093d4ab69b089bed69f3a95c18702b149677456`  
		Last Modified: Tue, 12 Nov 2024 00:56:12 GMT  
		Size: 3.3 MB (3253396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f200e326faf2829264325c88b94bd10bd3d73a6c26364ec4206695b135b88bd1`  
		Last Modified: Tue, 03 Dec 2024 22:42:41 GMT  
		Size: 294.1 KB (294076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eab153b4468df7f657167533fa78804e60b235edee0f04ec5dcc52a35b056da`  
		Last Modified: Tue, 03 Dec 2024 22:40:01 GMT  
		Size: 73.0 MB (72969813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef247b4f2967e59698556453c46baa232d92eafa942c7c62a90c7aa7dc6bb0b`  
		Last Modified: Tue, 03 Dec 2024 22:42:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:9c9078433ae03123930ea24aefec4477eddf199597c9ccb33e67dd551d2f7d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 KB (235939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe21017736946f8b931ebddb97160e51906101a72982400f345fcb826ab2298`

```dockerfile
```

-	Layers:
	-	`sha256:59f8ba51d7214aaea2d9191452ec8edead72058d48a4edc9440ffe897ed3b68c`  
		Last Modified: Tue, 03 Dec 2024 22:42:41 GMT  
		Size: 211.1 KB (211089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ecb8787c054087195c64923299e290e06ca5f9a425378c0c7907e8fd229a2ab`  
		Last Modified: Tue, 03 Dec 2024 22:42:41 GMT  
		Size: 24.9 KB (24850 bytes)  
		MIME: application/vnd.in-toto+json
