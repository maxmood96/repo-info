## `golang:tip-alpine3.20`

```console
$ docker pull golang@sha256:d096f58baa25284cd99535e63f0368c8b2717de5fc8bfe26410c7802018c39c0
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
$ docker pull golang@sha256:a5e3d32b3da86a35c586e9b47807e3158d94651fecacbb11c5fc7419cf6c943c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.9 MB (129887220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3880c16dfaed3ffd13dbfd4ce629b99eb1951106df22602d44afea01ca951b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 17 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0676395d002614980df8644df0b5c2543c7d0d5c9c9a82ba677d0182d11610c2`  
		Last Modified: Mon, 17 Mar 2025 21:13:24 GMT  
		Size: 294.4 KB (294372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41a83b25ec0e0c49ecd36fb9980281b7ce15ce7da6877f867a2e7766c298175`  
		Last Modified: Mon, 17 Mar 2025 21:13:26 GMT  
		Size: 126.0 MB (125965793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54d9d70287d23d9bd46de1a54b7ad471fd9d04fb86974d779c37eb9e99e4783`  
		Last Modified: Mon, 17 Mar 2025 21:13:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:9104788cac7a34e38b0745455de79f4a6c085aa952383d574f8a47df61ecba35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 KB (229867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7d2fd6b56bd86ad9fee6aff7fbc2dca1e507e16251f8dcc3c6d2d726c0c0a0`

```dockerfile
```

-	Layers:
	-	`sha256:596beef893fe29ade28054a0c0bd7e8c810e4383670827d80f3392de8dd5527b`  
		Last Modified: Mon, 17 Mar 2025 21:13:24 GMT  
		Size: 205.4 KB (205355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ec153b8cd9a6f496def7ddef4b760a650481347c55befd5f0a19f169f4fdf61`  
		Last Modified: Mon, 17 Mar 2025 21:13:24 GMT  
		Size: 24.5 KB (24512 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; arm variant v6

```console
$ docker pull golang@sha256:fee9e124d7b7df0e392f433a560badbc48285ee2adc1526a7cea03e84caffbad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124911850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8c107d18d519fd2c1a9a4ba5d962069555aa8fba7319576c20d1e5be26f2214`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 17 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
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
	-	`sha256:c9aedc9d4e47fa9429e5c329420d8a93e16c433e361d0f9281565ed4da3c057e`  
		Last Modified: Fri, 14 Feb 2025 18:28:14 GMT  
		Size: 3.4 MB (3372531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737183f74dc0d53c3f643812192622c6f3f2d83b37c68a4ca351085678413983`  
		Last Modified: Fri, 14 Feb 2025 22:17:11 GMT  
		Size: 295.8 KB (295833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3b09b35c999cf106d7ea623032afd4055be03b660fb3033618d47d166fe8b4`  
		Last Modified: Mon, 17 Mar 2025 21:13:06 GMT  
		Size: 121.2 MB (121243328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62000e71ac6c92f6bee66c1026f7e193a95fc26e8d63d2b27b0add9009e6f69f`  
		Last Modified: Mon, 17 Mar 2025 21:16:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:d9ff20b7bb7ea6b1cec3af5d8a851bcca5b283c3b22cf376891345db3caa15e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f2c906378c8040d7a8afee13291edb2a2a33c02f2a98859fd9e134b77fea58`

```dockerfile
```

-	Layers:
	-	`sha256:8e33bccc29241cfd601947da6233afac0e1c4bd6f7ad1a1aba3a6d425e0e4e6e`  
		Last Modified: Mon, 17 Mar 2025 21:16:20 GMT  
		Size: 24.4 KB (24405 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; arm variant v7

```console
$ docker pull golang@sha256:9f3d1b4ab3cf4b325a687406886b876c42d19922f953fa6668b55dbcca368975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124293133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a81078ac5edc5c1fd151292b982ab9b428fa92187e4378ace2bf5d1267b9c4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 17 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
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
	-	`sha256:772078ddbdee5be52d429e08f953aaad6715a90d7e4d6496eb1cd4004efa8a95`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.1 MB (3095969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d221261a6f80d203497a55ccecdc4912512b230fd036ba2df848b8144d67bf`  
		Last Modified: Fri, 14 Feb 2025 22:11:53 GMT  
		Size: 294.8 KB (294754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9907731a808176d84faa4a85282ae07e6a64aaf01c56d48e45253723c692ebf9`  
		Last Modified: Mon, 17 Mar 2025 21:14:18 GMT  
		Size: 120.9 MB (120902252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba89ea34540d007dcdda63e7a7328fcae5cdb1efe4417aa5e4f7bba0f5e9e01`  
		Last Modified: Mon, 17 Mar 2025 21:14:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:58f12684ac5450bb9674fb9c1b8aae67092b8d0f972efa44b344f82b56678517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 KB (229955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:351c6ea8d67eec755e4655cd4b4e4146a99e503df569d5f0f6117c7d389d100c`

```dockerfile
```

-	Layers:
	-	`sha256:49512afc74fdab10be62f3f6fc7da7c0405de19a8c7e67faadb5b628e9c04e94`  
		Last Modified: Mon, 17 Mar 2025 21:14:14 GMT  
		Size: 205.3 KB (205335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77810390758189300839634264fa64fba9f539d7525d61f7fff8ac31f9ba1b1a`  
		Last Modified: Mon, 17 Mar 2025 21:14:14 GMT  
		Size: 24.6 KB (24620 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:f56905f2a32fad37050a1399927f7e2dd5cc09f9f9d9fea336b1a04143b25ea7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122892659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ce2e4a0bdc588a39532af89faddfd57ee3ed4d98d3ebb9584344b976e7c7cb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 17 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
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
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345fe9f21930f1ad631fade17247453f42f8ccb115d7fa4ce0f092552a980ce9`  
		Last Modified: Tue, 04 Mar 2025 00:46:43 GMT  
		Size: 297.5 KB (297470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33fec41d8cea8d405aa42d9093a8aac6c3163d9643759441cd5e55b364f8ad55`  
		Last Modified: Mon, 17 Mar 2025 21:14:15 GMT  
		Size: 118.5 MB (118503866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12da2c38b24edd4d8661bcc68c1c7e1244d3f2506a23c9bddcd0d5793b19953e`  
		Last Modified: Mon, 17 Mar 2025 21:20:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:69a9189e1816e3bd3d81b28abd1516c7aa988c49bf61997d1119196ac0bd4583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 KB (230035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53f25611b9214b7dfc2e428b912c4fc8e1c2f0354454e0d4d3083978256e59c6`

```dockerfile
```

-	Layers:
	-	`sha256:760fb6d484ba9d7ab98e403194ec25449f74866f88c3f1fca302e21f29ed2d38`  
		Last Modified: Mon, 17 Mar 2025 21:20:40 GMT  
		Size: 205.4 KB (205387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7daa733d8d14065fe96dfddc547e361621cf5dbd926d2a9f847aef9a6a9b41a`  
		Last Modified: Mon, 17 Mar 2025 21:20:40 GMT  
		Size: 24.6 KB (24648 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; 386

```console
$ docker pull golang@sha256:0e876aa2e78308101f88453e1c60932ed31468a3ec99ac68f5e5ea65bb880015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127835535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6002f9b48066b79e2b08842663aa52a24640845051ad831c75e754c22e7ef58`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 17 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
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
	-	`sha256:b3d7db73e90671cb6b7925cc878d43a2781451bed256cf0626110f5386cdd4dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.5 MB (3471668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85905553579c4d6f7d96b316a0d20bc262050c8062e330596bfd845a7368bda0`  
		Last Modified: Mon, 17 Mar 2025 21:14:00 GMT  
		Size: 295.1 KB (295129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a94495553b1c250ac72571d6400e4136caa9f00d345a28d3faea166cf26f298`  
		Last Modified: Mon, 17 Mar 2025 21:14:00 GMT  
		Size: 124.1 MB (124068582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0ec2f58d7fa9b3457cf9aed72b8abe62fd4eb0f032033d0e3df570c3be76d2`  
		Last Modified: Mon, 17 Mar 2025 21:14:00 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:c142e3a195251819a40f2fc261134754a1a94304e6ce508f999812cc2807dfa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 KB (229779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48e647c932f36cb3ed87f97436662ba09eb009595944fb4ca7238b799893c01`

```dockerfile
```

-	Layers:
	-	`sha256:d53cd122ba340437556f297ca6fa15cd6b1036835ab46626efe51d6a62b887df`  
		Last Modified: Mon, 17 Mar 2025 21:14:00 GMT  
		Size: 205.3 KB (205300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5176e54e35b7f63f8e329ecc2632f575544d53c5aa12143afaf876886e7a2945`  
		Last Modified: Mon, 17 Mar 2025 21:14:00 GMT  
		Size: 24.5 KB (24479 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; ppc64le

```console
$ docker pull golang@sha256:a7d049b251f8ffa432d4068c793d7e42fc84cc7af647f66c7f297ed43d2f907e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124667286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad639353afdee12967c9ab11522120b417147ff526de9bdf34e97acb6fed6968`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 17 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
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
	-	`sha256:c9813c0f5a2f289ea6175876fd973d6d8adcd495da4a23e9273600c8f0a761c5`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3575680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed507fc5d64b2e3137d471f9a078a4add3c6cf38450cd6a53d7d3aef6ffec60`  
		Last Modified: Fri, 14 Feb 2025 22:08:09 GMT  
		Size: 297.9 KB (297887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c78cf9a0739a8dae1dc72464edfce0456a58eb76be29f8acb49a502b699b46`  
		Last Modified: Mon, 17 Mar 2025 21:15:53 GMT  
		Size: 120.8 MB (120793562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37398b2913b4d1c01994fa908c51d548d0fbda0f6b7bb7c802f62a9ce16b24d3`  
		Last Modified: Mon, 17 Mar 2025 21:22:18 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:726b670bd0f7d59918c4e543d7755278a2aa5b8eddef0effeb881f1d74aa8635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 KB (228024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b3319ce8a5044a428906680ecca4e5fccccefd04eec49662c35f2f4e73ddab6`

```dockerfile
```

-	Layers:
	-	`sha256:8f1644ff7364e8c21f1ad354445d501eed7404ec0c6695ad94cb7d3756165941`  
		Last Modified: Mon, 17 Mar 2025 21:22:18 GMT  
		Size: 203.5 KB (203466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d00da7031d140a8dfb1c4bdf6ec560ffb033ee4ac60804742aa1c0665a96552`  
		Last Modified: Mon, 17 Mar 2025 21:22:18 GMT  
		Size: 24.6 KB (24558 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; riscv64

```console
$ docker pull golang@sha256:40d3b2f335ccaf0833322d1eb474da87454813c2e4535f1dc4dad0cdf6c1e229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124784919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd7b13875674b7b334cf5300216d00b809cde024e88cd4f1de1502d28024160`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 17 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
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
	-	`sha256:69ccf1207daf2e3c381041f63cfe024189987fde3b1e97110475a71eac2581ba`  
		Last Modified: Fri, 14 Feb 2025 18:57:42 GMT  
		Size: 3.4 MB (3373232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12fa0de6a35b9467baeb7b28786dc580aa911bf02b2cc33ac7a44500327139a1`  
		Last Modified: Sun, 16 Feb 2025 06:13:57 GMT  
		Size: 295.4 KB (295446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae23c3d122e10f89f67d5f0d04fc58493a27c641b4150f620cf4c1351b302229`  
		Last Modified: Mon, 17 Mar 2025 21:54:02 GMT  
		Size: 121.1 MB (121116083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2799dbbc654d878113b2abf6c992ffa5a5e8d8d275fb11b64598f4c3ab62b439`  
		Last Modified: Mon, 17 Mar 2025 22:31:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:6c175b7f4c483741e6ec148704976ca1689a69ef032944628176da185fccd299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 KB (228020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a015224d8b890b530f31e6e560ebd1bfa1172f4360b338bc66369291a3fc39`

```dockerfile
```

-	Layers:
	-	`sha256:b7762c4e0a8d72321c2a834a2588ab36e2da88bc072fc3f3345143e03e1ff71e`  
		Last Modified: Mon, 17 Mar 2025 22:31:05 GMT  
		Size: 203.5 KB (203462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2c0ca68aa57f4609c8ea0f2ec5e4c27ada1b0c1d59218d3c21c1730161f9620`  
		Last Modified: Mon, 17 Mar 2025 22:31:05 GMT  
		Size: 24.6 KB (24558 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; s390x

```console
$ docker pull golang@sha256:e2e479e19b1ef3e6c10ba0e6ab50c8d8a4846846eb112aa859e2bc81b38f39a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126894618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d5110bada8b5b20f2902a3c27b978a1d9f481fce2462c9f69336a6bf1eb9ec4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 17 Mar 2025 05:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
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
	-	`sha256:7c6bf3be7c8016421fb3033e19b6a313f264093e1ac9e77c9f931ade0d61b3f7`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 3.5 MB (3464123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4709930918ff9545f85bd2e4cac3925cbdbb8c11ea2e9a6b1dfe4c10549f601f`  
		Last Modified: Fri, 14 Feb 2025 22:45:22 GMT  
		Size: 295.7 KB (295701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d46e335600bdcfe68156442397e360bf7b9f4f575af2fecc2a06de9129e542f`  
		Last Modified: Mon, 17 Mar 2025 21:54:19 GMT  
		Size: 123.1 MB (123134636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac71f1f164bc6680f703a4823f9ce56d46a07f1039255891353cc789303aa7d`  
		Last Modified: Mon, 17 Mar 2025 22:24:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:a3e6eccd3e3c27be2cfe64cb60c38e0821e8175f6520b2ffc8a91c2663502158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 KB (227916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df91d67386fea5f396bba5aeaaaa1c6b36fb18602970e343fdc865d77d869d1`

```dockerfile
```

-	Layers:
	-	`sha256:66529f6ddfa8300de9417bd624e768d3ffe299e53dcde49e3948d7031f20e25e`  
		Last Modified: Mon, 17 Mar 2025 22:24:06 GMT  
		Size: 203.4 KB (203404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ec2a4684bfe34e366038b1edc367c6eb051406144419d7eae8439fdbb759c4e`  
		Last Modified: Mon, 17 Mar 2025 22:24:06 GMT  
		Size: 24.5 KB (24512 bytes)  
		MIME: application/vnd.in-toto+json
