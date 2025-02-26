## `golang:tip-bullseye`

```console
$ docker pull golang@sha256:5b7bfdcbb311d21fc9c0ffe698ee36129f581dcd608ded84b781ffd5d464285c
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
$ docker pull golang@sha256:65f6a3265e5b0a8dd19ec0007ba63516b0c0c045d2a3c651b6995c41809c7d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.8 MB (339767600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78b55a131f7db73ac4edf74f90c451f352d616221c5b4c3ff9b66457e524cb20`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOPATH=/go
# Tue, 25 Feb 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Feb 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4ff5a3a54264ee833e4a09583363bbe779e881f15449fe4f4a6a662885dd37fb`  
		Last Modified: Tue, 25 Feb 2025 01:29:47 GMT  
		Size: 53.7 MB (53741401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6bcbc2151ce4be9aa40b26468719dafd6528d7d11d6f6cb60e3a58a3447305`  
		Last Modified: Tue, 25 Feb 2025 02:12:52 GMT  
		Size: 15.6 MB (15558424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e36295709cc3855d0f98f8a6b939053cc43efcf3092756703c1fc518d73fe77`  
		Last Modified: Tue, 25 Feb 2025 03:13:48 GMT  
		Size: 54.8 MB (54752085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33139b79e0c745e410a525fd83ec451a64fa02d39d1f344798142f111dc1272a`  
		Last Modified: Tue, 25 Feb 2025 23:30:40 GMT  
		Size: 86.0 MB (85971680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a93651a1e507b5bd3cfde19fbfc91acf223de81d90d9e07fc812851aad09e7`  
		Last Modified: Tue, 25 Feb 2025 23:30:29 GMT  
		Size: 129.7 MB (129743852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7164ea6758679f758f2cae6f5396b1390f6cab2ddd178680232bd15a8ff92b1`  
		Last Modified: Tue, 25 Feb 2025 23:30:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:14b9ef1f0816d4fafe67bae828bc2a49584ccc655b0b512223d6e1bc120bc163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10291346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7aecab7e9b4c55f9135475f34cf4ad1179979462f38355383334038e7a83029`

```dockerfile
```

-	Layers:
	-	`sha256:2ba1d6b650f35634bfdef96a83ce0c5b1d697dff917d6a5a0c545ac2e6d315ee`  
		Last Modified: Tue, 25 Feb 2025 23:30:39 GMT  
		Size: 10.3 MB (10264285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7ce3143df87072754bb13c91ae382ac8617fa99918051888dc04649a53c8403`  
		Last Modified: Tue, 25 Feb 2025 23:30:39 GMT  
		Size: 27.1 KB (27061 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:1787bb7b51009740e3c3623dc2bd93f608131269d15e6ce5b0d629e111f5e7db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302268881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fbe5eafaa069e4a26947be1ef0167e8a5933c79aae12c9ce1d4c7f8aa34eb42`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOPATH=/go
# Tue, 25 Feb 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Feb 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
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
	-	`sha256:cbe77fa27af7b36c34f8f11e6bd2bd4b9ddf9e28c094fdee1cc3b2735243e847`  
		Last Modified: Wed, 26 Feb 2025 02:56:52 GMT  
		Size: 123.0 MB (123034972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6feded03f0c974f891c7f873f2a44a5b43ab8cedb6aab734975cba4bf3f7809`  
		Last Modified: Wed, 26 Feb 2025 03:00:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:2ba0b3e8766d10c79054a1c03f6071f8a1dd58b3a43e3b68e44b014fb337e6d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10097794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ace22b412a8d1174f599e2edbd436c375982b1bdacf89ec5517fb4a2d6dc70e`

```dockerfile
```

-	Layers:
	-	`sha256:e18567f7183a0253f50d3aa042f5e42680628c318755d75e72cac6f285f4879b`  
		Last Modified: Wed, 26 Feb 2025 03:00:10 GMT  
		Size: 10.1 MB (10070625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d305ed1acb45398876a93a0eaed1f725be1c8e1a080710a15ae2e6e8feecbf8c`  
		Last Modified: Wed, 26 Feb 2025 03:00:09 GMT  
		Size: 27.2 KB (27169 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:8a727026cd5fb3b732e347a6ad21ae3db8034c19b9683ace79fd3e468f01fff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.6 MB (326595744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8027b28b2a976a9cc20f4ecf8d8ff2fe97abae55011ff8855d0c796bf58355b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOPATH=/go
# Tue, 25 Feb 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Feb 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
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
	-	`sha256:2614c2a3e3d51531f3e6054729bc451d46f9dc5a940312857ed35b9f27a5d5aa`  
		Last Modified: Tue, 25 Feb 2025 15:29:12 GMT  
		Size: 81.4 MB (81382606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e46df0fcf6e0e573af560112ea65411de1e4c09446bfe2aa5c396181b055ef`  
		Last Modified: Tue, 25 Feb 2025 23:43:25 GMT  
		Size: 122.6 MB (122564769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3da1d74df59a5cb45957273afe11aa038546db5cc8da891a0cf630d2b3e540`  
		Last Modified: Tue, 25 Feb 2025 23:45:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:40f7adc27425cc41a4f82b495f143f8f7f34490e2d6753a23b101c624f31b1bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10293054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:305032ea6dbae3360448726813def25ff63fa358b6e41fbf7deb4907869f276b`

```dockerfile
```

-	Layers:
	-	`sha256:3a2bf80edccd9911298e5ca5cfcd4d006180677b0a65d4c072cfe94e97fad462`  
		Last Modified: Tue, 25 Feb 2025 23:45:35 GMT  
		Size: 10.3 MB (10265857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8503a3473e0178589942aba83bc660630555b6612a5b09064cb9891422f08015`  
		Last Modified: Tue, 25 Feb 2025 23:45:34 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; 386

```console
$ docker pull golang@sha256:de0dd990a7b900496be31ce2639e290a6a2683c4cc00fe508ddc3c0bd4202e20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.6 MB (340572254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4085e759176cc6119ab806d372166a98fca91b91241f9aaef2cb657970fbb25b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Tue, 25 Feb 2025 00:23:21 GMT
ENV GOPATH=/go
# Tue, 25 Feb 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Feb 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 25 Feb 2025 00:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7d167bff82d228d113e8b77cccc9449d0007cd097723599b66c8772979708da8`  
		Last Modified: Tue, 25 Feb 2025 01:29:52 GMT  
		Size: 54.7 MB (54678863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1763bdfcd7e692c8f35c71602a5206ff9e4716856edf6ae712febb4cc579d3`  
		Last Modified: Tue, 25 Feb 2025 02:24:11 GMT  
		Size: 16.1 MB (16062177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820de11811e966e41fc39b6790cf28a33ce0645127033d9f041fa3707235430e`  
		Last Modified: Tue, 25 Feb 2025 03:13:43 GMT  
		Size: 56.0 MB (56030023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e6ba80025c100a8947685d42ef4906cc291f0918abec00d7184faa4c24f76b`  
		Last Modified: Tue, 25 Feb 2025 23:31:11 GMT  
		Size: 87.4 MB (87398241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ea1fd7113951d2f0ff9a9824c4749a117ae67be28d96b0ab33e27305a83954`  
		Last Modified: Tue, 25 Feb 2025 23:31:02 GMT  
		Size: 126.4 MB (126402793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394b4a6a28e3c9e8a03e765d143aaef564c12d701bae6cca06a993ce3d4c87b2`  
		Last Modified: Tue, 25 Feb 2025 23:30:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:ea2f6da043762d6667378301b7d45f1df2bf26ce9d9a45412aa3f9fcf6b02aee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10281104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6190338b086b89a6c826fe1e429afb8c26e40b9c2539584047dedfe11e6dac4a`

```dockerfile
```

-	Layers:
	-	`sha256:b77a0b2c8bbc608b06ce50ce391a36f1003771b0b1e8dfa803242af8653ab89e`  
		Last Modified: Tue, 25 Feb 2025 23:31:09 GMT  
		Size: 10.3 MB (10254076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c054c07566325c52984930ecae8dc4d05e663ea2c9983226d28c1cec24edd1f`  
		Last Modified: Tue, 25 Feb 2025 23:31:09 GMT  
		Size: 27.0 KB (27028 bytes)  
		MIME: application/vnd.in-toto+json
