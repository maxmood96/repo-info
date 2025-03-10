## `golang:tip-alpine3.20`

```console
$ docker pull golang@sha256:0d9afc77998ccab7a1a5d41c71b90a4530760c0d669b147c173c64b0f1318707
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-alpine3.20` - linux; amd64

```console
$ docker pull golang@sha256:894966ae68c10f43663285f0c8b5605750abc3a5f48624a1cb5b5482af70b5e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (133978328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f693efe12ca0e7af9da0d89e7320d7448d15648be9795850c420f3f2e8ff280`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 10 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f5503906315237dadc55587baa4b60c72607fdee16133d03f1e08de930d799`  
		Last Modified: Mon, 10 Mar 2025 21:08:31 GMT  
		Size: 294.4 KB (294391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebef8b724b3fa04791227bd9b0114cdd3af9884886d8745737430beaa3ca50e`  
		Last Modified: Mon, 10 Mar 2025 21:08:33 GMT  
		Size: 130.1 MB (130056881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3adcbe8660c4263a085aac576cdac03eb62c0f2465a47eeb947bcb1d0a0ebf73`  
		Last Modified: Mon, 10 Mar 2025 21:08:31 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:4d367b0fb0726cd922549d1b5fbc8d4befa22e6df20c7e4da91fb743c6fa461c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 KB (229867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4050fe2d8a8db3e0aa196503b44168ee1cf857b5a3be6f20438da805fb77e8a`

```dockerfile
```

-	Layers:
	-	`sha256:a80a1ae2144bea8885e44d6bcf2f05ceebf4a27662951c2d13d29775d21ee228`  
		Last Modified: Mon, 10 Mar 2025 21:08:31 GMT  
		Size: 205.4 KB (205355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74870405ab0773a9254bf5e6b45b6a8834f8bc0b26658de0bb48894a871956e3`  
		Last Modified: Mon, 10 Mar 2025 21:08:31 GMT  
		Size: 24.5 KB (24512 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; arm variant v6

```console
$ docker pull golang@sha256:19526766c883304cea46057f9c2e9a8725a9d452a85247b4af5b23a94dad688a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127272231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691daff88bf578471ee93110bb8f776261a5d6a6cc5dd3ce85b8b8e4999472c1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 10 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
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
	-	`sha256:c9aedc9d4e47fa9429e5c329420d8a93e16c433e361d0f9281565ed4da3c057e`  
		Last Modified: Fri, 14 Feb 2025 18:28:14 GMT  
		Size: 3.4 MB (3372531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737183f74dc0d53c3f643812192622c6f3f2d83b37c68a4ca351085678413983`  
		Last Modified: Fri, 14 Feb 2025 22:17:11 GMT  
		Size: 295.8 KB (295833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ce17012293f93110ff830a12cfb6a99908559d195b72085742e8f7d74c9458`  
		Last Modified: Mon, 10 Mar 2025 21:07:20 GMT  
		Size: 123.6 MB (123603709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ae186235f91f12c27689f1589088df4f7451f0d0265babe9e5e5ecabc423b8`  
		Last Modified: Mon, 10 Mar 2025 21:10:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:728b5a6f50133e394283bc3919413c508e0ae59f2f2a3f26162be63a5ce4f648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc5d8c0f95727ac4d37c22180814cb68e0e2c67a8c2d1e874ea4c489976e468`

```dockerfile
```

-	Layers:
	-	`sha256:c80bc483561730fda5a683cbf01b08ba7e5208bd2c92004377e25799691bd0ca`  
		Last Modified: Mon, 10 Mar 2025 21:10:42 GMT  
		Size: 24.4 KB (24405 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; arm variant v7

```console
$ docker pull golang@sha256:cef4c8c3fed121118ce89f8649af0392168233e3eaeae535daf8228cf475b1e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126664777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771c0cbde784a9018e0b844d00e6910c8f8913c6a58b6f89f9563d223237fe61`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 10 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
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
	-	`sha256:772078ddbdee5be52d429e08f953aaad6715a90d7e4d6496eb1cd4004efa8a95`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.1 MB (3095969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d221261a6f80d203497a55ccecdc4912512b230fd036ba2df848b8144d67bf`  
		Last Modified: Fri, 14 Feb 2025 22:11:53 GMT  
		Size: 294.8 KB (294754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca61e995b8c13d851dd3e3c6f227fdb4c36ab271e17ec8b18961597fba4895b4`  
		Last Modified: Mon, 10 Mar 2025 21:09:26 GMT  
		Size: 123.3 MB (123273897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60fd9944d7bc25a37d4233583f331548538b7e168d51dfae507701b9990002e8`  
		Last Modified: Mon, 10 Mar 2025 21:23:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:9ae24c1f7def9e3db3a08760548c8f6b9d3f396ddf2195f934b5c4f2f73dbea1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 KB (229955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfdfe860eff09d77be1fb0e5aac865b616738f4125a0bf2fa44c9200dd5f8495`

```dockerfile
```

-	Layers:
	-	`sha256:2222cb1ea0caf1d9580b7c33794c740bb52a2f5c3025469c784f4c1a84c915a1`  
		Last Modified: Mon, 10 Mar 2025 21:23:16 GMT  
		Size: 205.3 KB (205335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ae87d5cfa1bd06afbdce3241f42dda7899184421c0db56d4254675a08397466`  
		Last Modified: Mon, 10 Mar 2025 21:23:16 GMT  
		Size: 24.6 KB (24620 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:aed15c50f21bc634dc2cde0bbb95d3541aed8bdf020a069ab6b613b279a695c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127186815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded1372532db87a79ee4478494e09f36bd0e459a24c37c19ebb4d2177beb3ba1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 10 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
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
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345fe9f21930f1ad631fade17247453f42f8ccb115d7fa4ce0f092552a980ce9`  
		Last Modified: Tue, 04 Mar 2025 00:46:43 GMT  
		Size: 297.5 KB (297470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e9a129027ad3875ac19234bac00390ebdd61f752809a25128556ac5b500a6c`  
		Last Modified: Mon, 10 Mar 2025 21:42:38 GMT  
		Size: 122.8 MB (122798022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e2b653e943ec903ac10521b95785e42b3c94d90966d840ad5c68cecbd13329`  
		Last Modified: Mon, 10 Mar 2025 21:54:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:2ce24b866728f2c6c7b6fafe64d8c8488555b3735763e42cce4da98333928b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 KB (230035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f1d5488d9f93cbd1b5f7b268f081c62cb25b870dc9dfde914dd77e6906e875`

```dockerfile
```

-	Layers:
	-	`sha256:cb09583c15e4357330117c9efecec5dc2eb98988f3235c02cff5469e81237896`  
		Last Modified: Mon, 10 Mar 2025 21:54:29 GMT  
		Size: 205.4 KB (205387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfbadf1735164b3c7f8db62f21f249ba8040687989c6dd5208a0c95cbb449b0d`  
		Last Modified: Mon, 10 Mar 2025 21:54:29 GMT  
		Size: 24.6 KB (24648 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; 386

```console
$ docker pull golang@sha256:a3ac0ef0309897ce167912985948adc0cee1d8a13c0af982efc4e5823ebae6f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130422812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75181e1582563d213a175d4cc8f06c142f902f38b528af651f7d49f23a5f904f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 10 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
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
	-	`sha256:b3d7db73e90671cb6b7925cc878d43a2781451bed256cf0626110f5386cdd4dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.5 MB (3471668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba737df2ab6499318f67eacfcb3a247add0409ec2ef7796168cb5c5ea21a5f4f`  
		Last Modified: Mon, 10 Mar 2025 21:08:45 GMT  
		Size: 295.1 KB (295141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae7ca0102091a7eba5053fb3365f646b5b1d1473c73f95b22ed69abf7ea5a21`  
		Last Modified: Mon, 10 Mar 2025 21:08:48 GMT  
		Size: 126.7 MB (126655845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3abef73f0027afac55da35e528ef2d5486ae459debdad2c42626ff8dbef9d4e0`  
		Last Modified: Mon, 10 Mar 2025 21:08:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:5a27a71f5564bfdde603ca93fa2df565bea2193beec8751cb73ca9c39e6be93b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 KB (229778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f76f0329e371fd54282278aeae9651625360bb35dd2459e16d5e49954f324f2d`

```dockerfile
```

-	Layers:
	-	`sha256:8b5bc38afce749ee82b767adf2f2e65db178ad10598fa3df07c439c2d0c40667`  
		Last Modified: Mon, 10 Mar 2025 21:08:45 GMT  
		Size: 205.3 KB (205300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0e020c101882c1da237f2a9124e3d298dd8efb53837377da026c57d1da7711d`  
		Last Modified: Mon, 10 Mar 2025 21:08:45 GMT  
		Size: 24.5 KB (24478 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; ppc64le

```console
$ docker pull golang@sha256:2e5ee2c61db018ae337b523079e03dfdcbad6e6ef5bd1b816e57932f83dd159d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129072722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e85e87e4c1fc8e4345a7da0b9973f82a6aa4d27e061b454013c71cae64e287`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 10 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
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
	-	`sha256:c9813c0f5a2f289ea6175876fd973d6d8adcd495da4a23e9273600c8f0a761c5`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3575680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed507fc5d64b2e3137d471f9a078a4add3c6cf38450cd6a53d7d3aef6ffec60`  
		Last Modified: Fri, 14 Feb 2025 22:08:09 GMT  
		Size: 297.9 KB (297887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34eb0a545ff499f8c9f925571d19e4ecfc63b1db1f51e83434ef213b02ed36ca`  
		Last Modified: Mon, 10 Mar 2025 21:27:32 GMT  
		Size: 125.2 MB (125198997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ef8edb4fd0c4765c56801b2acbfa2525a5cea62128a5f3c0111c0459577126`  
		Last Modified: Mon, 10 Mar 2025 21:27:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:02e7caa9e3d1dedb4a371d570228353c325bdde024bf0fc8a956f5fb640d61a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 KB (228024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250f77a15c5d058c1b12aa61b2e94f7d788c518a4e37dcb1f603eaa1021404ae`

```dockerfile
```

-	Layers:
	-	`sha256:fd96118b4c6125634c88fd20b0295eb58f4c74fa4dec07fea26c0d0b2adf6992`  
		Last Modified: Mon, 10 Mar 2025 21:27:29 GMT  
		Size: 203.5 KB (203466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b5d9b6f9712dcc0ed686ab47dce404af91e1f7798be3e53da65148bfd996519`  
		Last Modified: Mon, 10 Mar 2025 21:27:29 GMT  
		Size: 24.6 KB (24558 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; riscv64

```console
$ docker pull golang@sha256:6f0b105c7ff1138c7deab102ffd447b75bba63fe33f8d8493a6132e6f9575242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.3 MB (129281721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccae3284dba988340bf42a404a83c261a83e822f60993a9b75f1e85ee501be14`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 10 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
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
	-	`sha256:69ccf1207daf2e3c381041f63cfe024189987fde3b1e97110475a71eac2581ba`  
		Last Modified: Fri, 14 Feb 2025 18:57:42 GMT  
		Size: 3.4 MB (3373232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12fa0de6a35b9467baeb7b28786dc580aa911bf02b2cc33ac7a44500327139a1`  
		Last Modified: Sun, 16 Feb 2025 06:13:57 GMT  
		Size: 295.4 KB (295446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6729a0f61bbc9e575471b77c64d66e78707d0b2ef93e51eb592124ffaea0df`  
		Last Modified: Mon, 10 Mar 2025 21:47:43 GMT  
		Size: 125.6 MB (125612885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad153760bb393bd2fb3dd55b3c0f7bc2806c5b8d48fdad17f0026b5a03541afb`  
		Last Modified: Mon, 10 Mar 2025 22:24:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:7f6507315e7e8132d7e9039d378b99a5d46e47ded45c542762c2a1ee12141d06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 KB (228019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c6aedf385692a456e86391bacbbb20c1ffdf324ecceaa34bb33c0c7968244c3`

```dockerfile
```

-	Layers:
	-	`sha256:0cf93466ed7fe6c5a9a77d5617e8ead9f8ad4ae66c90ac7db124063a7cb25ea8`  
		Last Modified: Mon, 10 Mar 2025 22:24:56 GMT  
		Size: 203.5 KB (203462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f01fd43032012667c11f2894ef0f9404547a0f53a6b8fba8e7f28d6e648334c`  
		Last Modified: Mon, 10 Mar 2025 22:24:56 GMT  
		Size: 24.6 KB (24557 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; s390x

```console
$ docker pull golang@sha256:233965af187cbc7297641f00218162300a9dac0688d41bb18ded569af2757c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.3 MB (131319086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c123cd241ae7226a566eccd6dd068eeabb4adb02dfeb24a9399434b9ac8dd75a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 10 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
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
	-	`sha256:7c6bf3be7c8016421fb3033e19b6a313f264093e1ac9e77c9f931ade0d61b3f7`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 3.5 MB (3464123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4709930918ff9545f85bd2e4cac3925cbdbb8c11ea2e9a6b1dfe4c10549f601f`  
		Last Modified: Fri, 14 Feb 2025 22:45:22 GMT  
		Size: 295.7 KB (295701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eeba62321e032790263a70e54013602b15b70d9827bbb67e4e5c952c8d15c8a`  
		Last Modified: Mon, 10 Mar 2025 21:35:35 GMT  
		Size: 127.6 MB (127559104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2623f4269b3a5d9a34cbf7a1127095bf5e47f34564f6b8ce6cfa450e8dfc7a4`  
		Last Modified: Mon, 10 Mar 2025 21:35:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:6d5f2d364f7a1423023369f15b8656cc5591614c204bcf4a0337e2ce599c10e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 KB (227915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc3a151e65d6fd43c47bb994692ca9e62abded6677f65551159e11860c43521`

```dockerfile
```

-	Layers:
	-	`sha256:f3de7e84565e508fcac97a003ee5a6bb74192ef64a2114aab0d04d389ed4390f`  
		Last Modified: Mon, 10 Mar 2025 21:35:33 GMT  
		Size: 203.4 KB (203404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b14ea485377e1b6b139def694e01a64dcd3fa02850b83f5eed33f4929e15444`  
		Last Modified: Mon, 10 Mar 2025 21:35:33 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json
