## `golang:alpine3.20`

```console
$ docker pull golang@sha256:3d9132b88a6317b846b55aa8e821821301906fe799932ecbc4f814468c6977a5
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

### `golang:alpine3.20` - linux; amd64

```console
$ docker pull golang@sha256:e042fa2203bd9b3898d827bbb1c8633a0bcffdf18d73340e1b58a74b723fad3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82848517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15169d388306b86e1e95f29331329ad91d2176beab589245758c1d0498209b6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 04 Mar 2025 19:43:12 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOLANG_VERSION=1.24.1
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOPATH=/go
# Tue, 04 Mar 2025 19:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 19:43:12 GMT
COPY /target/ / # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56fce97e15ede677bac6c8825be8f2dedb8778716f62975387f2ea203fa5acd1`  
		Last Modified: Tue, 04 Mar 2025 21:17:44 GMT  
		Size: 294.4 KB (294395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178cc98ff0842a2601bbc4e7db3db70a323469849a03684d1b9b21e7f825b7e4`  
		Last Modified: Tue, 04 Mar 2025 21:17:18 GMT  
		Size: 78.9 MB (78927068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341e2350b6b0268713d7773629c8081b7d58dd19fa79ce20ff79487a08be78d5`  
		Last Modified: Tue, 04 Mar 2025 21:17:43 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:70600ff68ad41c95f07c03ad3ee0354639863011d5475d2055c9c6176c223482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 KB (234887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d91e34b38c3a37b5e46284cac942f683c357a206e88b1b9ed73e0219e1c62b`

```dockerfile
```

-	Layers:
	-	`sha256:f01ccf77509c3ef69c994697e64442a63634d746ff93f73a8f453f371ac763bc`  
		Last Modified: Tue, 04 Mar 2025 21:17:44 GMT  
		Size: 210.0 KB (210037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fabad28125e81467d2edc33aea110a8fb5c9e55616ae661bd839a8c679f87fb`  
		Last Modified: Tue, 04 Mar 2025 21:17:43 GMT  
		Size: 24.9 KB (24850 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; arm variant v6

```console
$ docker pull golang@sha256:cecb71b49204d0c226b998e081ba5b5689b9e62bf0a8179435d137091bc04034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.8 MB (80754595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08512d01338a9a78355c51ce322cc77391eba3998b7dfc45d8efb9d02a2fd0b9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 04 Mar 2025 19:43:12 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOLANG_VERSION=1.24.1
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOPATH=/go
# Tue, 04 Mar 2025 19:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 19:43:12 GMT
COPY /target/ / # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
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
	-	`sha256:4963be56d6d006d685712b5501f44815d69ae8f38e7bd0f798f9d6f75471c5cd`  
		Last Modified: Tue, 04 Mar 2025 21:17:06 GMT  
		Size: 77.1 MB (77086074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6951fecb41f22e44c00d1efa246d7ec0fc1c4604bbbb2a27e7fa003a05b1663`  
		Last Modified: Tue, 04 Mar 2025 21:17:33 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:c3e94efc7680bac75c1c442d0b2a6d3aceb255fe52695c0b61d02fb7e2944495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 KB (24736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2824a4394a915a0d8d0bb6bb2e452eab257a9152a05b1f1dcd3b37fcd1a4ed4b`

```dockerfile
```

-	Layers:
	-	`sha256:46e6ab26ab0334c275257d4d50117496ca62e0377f9f7fc03fab037b535f4807`  
		Last Modified: Tue, 04 Mar 2025 21:17:33 GMT  
		Size: 24.7 KB (24736 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; arm variant v7

```console
$ docker pull golang@sha256:7af40d96c76ab1d3ed3a58d242eade868092479531818e2b97e683dd4f412b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80477286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:006fbcf2628e67e76e6401ba0df3ef79011fdda92db34337321562c9ab57341f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 04 Mar 2025 19:43:12 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOLANG_VERSION=1.24.1
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOPATH=/go
# Tue, 04 Mar 2025 19:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 19:43:12 GMT
COPY /target/ / # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
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
	-	`sha256:942c762e5659795d4f6aaa827e039a42ab97a6e3ec651d1ff497332bb958710f`  
		Last Modified: Tue, 04 Mar 2025 21:56:10 GMT  
		Size: 77.1 MB (77086405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc19e694a1c5da2cdc1097f585c7ba73135904e1581dcecb918df697016b714`  
		Last Modified: Tue, 04 Mar 2025 21:58:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:74a2fdc346eee61d940264e7178bb075ea70bfac1f34fa42ac5286fbec893fcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 KB (234988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b14832bb40b1b7cb52f81282abf9b440011afbae3dfbce1183b414fed23d2b48`

```dockerfile
```

-	Layers:
	-	`sha256:547e51787afcd4a4b05895e7acff5a6a0e1e2e7dc3e65d2bb3b494c476345a29`  
		Last Modified: Tue, 04 Mar 2025 21:58:46 GMT  
		Size: 210.0 KB (210037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae9c4ad2053816d85b5d1baccb8719761805c5784091c909316655babe3db390`  
		Last Modified: Tue, 04 Mar 2025 21:58:46 GMT  
		Size: 25.0 KB (24951 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:958f3b598fd599b4bfc798bb30537ee47fb6f8e83883286d4105522fd9b81d62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79572803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb005c28626c6caf031875401efaf5e066663e64b1527ea8ebb99cb9441ee02`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 04 Mar 2025 19:43:12 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOLANG_VERSION=1.24.1
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOPATH=/go
# Tue, 04 Mar 2025 19:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 19:43:12 GMT
COPY /target/ / # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
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
	-	`sha256:57f2b93ee17017a4673f1a381ec312f22e8e9c0cee491adc746b10d3d5f200b7`  
		Last Modified: Tue, 04 Mar 2025 21:57:12 GMT  
		Size: 75.2 MB (75184010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b07b37c981415069c3f0584aa696f6f9ad3cf897049aa4a7d907715f5bafb3c`  
		Last Modified: Tue, 04 Mar 2025 22:03:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:c97b8977743f611bc44869ce0e055700c1345288dd1c80f7c2dfe23788f892fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 KB (235077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac16886137556de9bc05e1d2d5c881c96a39b38c16a20e80c0d9ad9b73caa7e`

```dockerfile
```

-	Layers:
	-	`sha256:4dec1a03a235412c5e1ec2b1e19d47b6e1163c75115bef6a2ac824c9a188e1ec`  
		Last Modified: Tue, 04 Mar 2025 22:03:46 GMT  
		Size: 210.1 KB (210093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5fafec9d5c26ba23251ebb379797a5daa2211b694cdd39679b1b69f64c52c82`  
		Last Modified: Tue, 04 Mar 2025 22:03:46 GMT  
		Size: 25.0 KB (24984 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; 386

```console
$ docker pull golang@sha256:766c66362a0ac88bd7d3268420cf2ad2f6cf53b074f7ae20c76cdfb7ab8167f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80627108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f76db59e2e88d1ccfff54e8063d7586498d643fa81438b818560d186b2231d6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 04 Mar 2025 19:43:12 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOLANG_VERSION=1.24.1
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOPATH=/go
# Tue, 04 Mar 2025 19:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 19:43:12 GMT
COPY /target/ / # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b3d7db73e90671cb6b7925cc878d43a2781451bed256cf0626110f5386cdd4dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.5 MB (3471668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b2bf05eecdc1e25ebb4eddf2afdad0454d8c502d6b65936fc30570e52e637d`  
		Last Modified: Tue, 04 Mar 2025 21:25:34 GMT  
		Size: 295.1 KB (295135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d9251e0d8de5337c7947faa7a74d8a5743e95d63c085ef6f4a9939b793d5e3`  
		Last Modified: Tue, 04 Mar 2025 21:25:23 GMT  
		Size: 76.9 MB (76860148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdd624c68f41a42f665651dfff24d3eba04c07b8757a92ab9c2c9ac18044377`  
		Last Modified: Tue, 04 Mar 2025 21:25:34 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:ba05de54c253bc4b8e9c4226ef2df31253d9d50452bb9a80198d95ee411873a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 KB (234790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93625518122d24f054d5b2144496d8388aff8af18f22d34a99247af15dc7829`

```dockerfile
```

-	Layers:
	-	`sha256:4264dda0e9af91909b01b4379c8def75fcfef907bba7654fbd2b91018aacfd5c`  
		Last Modified: Tue, 04 Mar 2025 21:25:34 GMT  
		Size: 210.0 KB (209976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66c036ad53586adb7b1307d7a92370b3f9816b1a25880eca473f7a7eba9e7deb`  
		Last Modified: Tue, 04 Mar 2025 21:25:34 GMT  
		Size: 24.8 KB (24814 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; ppc64le

```console
$ docker pull golang@sha256:d419053b5a054b8da0662221d751ec055cd5be4912f0a97e6f763406cd79b9f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79364267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53bfae24c81717a8ba9d2a4d201476fa7199b4088fb04a35b1dc14a9e1339615`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 04 Mar 2025 19:43:12 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOLANG_VERSION=1.24.1
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOPATH=/go
# Tue, 04 Mar 2025 19:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 19:43:12 GMT
COPY /target/ / # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
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
	-	`sha256:a5911afb128e3f71046cf878de8eec44c93ec9b167d4e1c0d275b0bb6705ba8e`  
		Last Modified: Tue, 04 Mar 2025 21:17:56 GMT  
		Size: 75.5 MB (75490542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7260bd0fe2713f053800795e76302db2f29e05cfaf46917d1897823962076386`  
		Last Modified: Tue, 04 Mar 2025 21:20:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:dd8816ec60a9ad4b29c2d3111643bf98932138b61dc263dafd4fd48edc9ec313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 KB (233054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f31c0b87be3401b1415c09e9b79ab5d32899924e3ed7f64d8fd8cd140db1cd1`

```dockerfile
```

-	Layers:
	-	`sha256:daed77a822e3a40b386e9fe74fc588cf75c9ca048e83bb3a7b4d23a1ac2fef76`  
		Last Modified: Tue, 04 Mar 2025 21:20:44 GMT  
		Size: 208.2 KB (208156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:824c4b6ca89df0c1a7d5d10d6868599d28e44d58c023754e9f34058a64e6af45`  
		Last Modified: Tue, 04 Mar 2025 21:20:44 GMT  
		Size: 24.9 KB (24898 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; riscv64

```console
$ docker pull golang@sha256:63394206dda99a76d4e29be4344485cfa0b9c38c47083ad90b7c431b92a33554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79936726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0d19fc61bd36446cf25ff18aadad0caacf2e067e0584b8f6e38de26c4241e1e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 04 Mar 2025 19:43:12 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOLANG_VERSION=1.24.1
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOPATH=/go
# Tue, 04 Mar 2025 19:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 19:43:12 GMT
COPY /target/ / # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
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
	-	`sha256:d23ea26c6de15331d7cbe251d829682bbe8cda453de3d96aaab22b8deaa009d5`  
		Last Modified: Tue, 04 Mar 2025 21:22:37 GMT  
		Size: 76.3 MB (76267890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5df6982f13f286813025e6379cc75db9daaafc3c7d2da6653ddab44a214d8a0`  
		Last Modified: Tue, 04 Mar 2025 21:34:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:95ef6eba9da0e9f5e891373656b31d6c3762d86fb51dac61c8678e728282223c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 KB (233050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0529fddf74faebbb36273f1a1db0c3e4f11a0384ba47f02e4c52ee6792e7b2d2`

```dockerfile
```

-	Layers:
	-	`sha256:bcb333a20d62e7a6e9c5e83b8f1f0fc2a6cfa12918b57d300a4f0a1792985003`  
		Last Modified: Tue, 04 Mar 2025 21:34:22 GMT  
		Size: 208.2 KB (208152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c77aeaadf03f3ecb9cd1be57d0769a74a7db84cef0b20b4fad19b51cf5dffc94`  
		Last Modified: Tue, 04 Mar 2025 21:34:22 GMT  
		Size: 24.9 KB (24898 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; s390x

```console
$ docker pull golang@sha256:5c4cd49a8fe14eb4ca1b8836f84bc588602740273adbdd49ead6331d3c3e2fcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81492827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e45b96e43a584294a0752894480f75bdff26eb0e85572fe5e9b5e7e7c8e04a3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 04 Mar 2025 19:43:12 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOLANG_VERSION=1.24.1
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Mar 2025 19:43:12 GMT
ENV GOPATH=/go
# Tue, 04 Mar 2025 19:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 19:43:12 GMT
COPY /target/ / # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Mar 2025 19:43:12 GMT
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
	-	`sha256:f8de37e33097ae1468a19882a2526d339560c4de2ed0728e2c2fccb5003120c7`  
		Last Modified: Tue, 04 Mar 2025 21:21:51 GMT  
		Size: 77.7 MB (77732848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9d949ccb00098ee69fb48759c26c3f42c309d911fde4f20afbe433f0df5ca6`  
		Last Modified: Tue, 04 Mar 2025 21:26:35 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:a748df60988e55621f78702349642410554e0d16228b43fe616c29037644841e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 KB (232936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:700b724c57359584a2d42e7e80bfd5f07f687cbb1d4bb3e6e991c9924e6115b7`

```dockerfile
```

-	Layers:
	-	`sha256:0ba822b4f61c7862c8d040072c5a4c4bca5a88f60203b9f68d30b4d27c19dfe7`  
		Last Modified: Tue, 04 Mar 2025 21:26:35 GMT  
		Size: 208.1 KB (208086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36c67c13e868a09869c9f781c4cd53a16fad6a3efbaa360f8374d1d00396c563`  
		Last Modified: Tue, 04 Mar 2025 21:26:35 GMT  
		Size: 24.9 KB (24850 bytes)  
		MIME: application/vnd.in-toto+json
