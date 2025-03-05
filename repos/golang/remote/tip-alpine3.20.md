## `golang:tip-alpine3.20`

```console
$ docker pull golang@sha256:8ac65872c0988757bb86d81a2af7cca29af11c4bbb6272ef4a19999f3df42aa2
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
$ docker pull golang@sha256:3f2f9306f875c22734176815ed1bd6e7bec019f05dc4927a430fdbc64e2f1f9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133760219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f61a8a89b0e793ef4a9955ebb0006d7a829cf87408a31a103acbf9756dc588e7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 00:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOPATH=/go
# Mon, 03 Mar 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Mar 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54cbad5d23ea19a47811c0027e3fda3c2ae012525070e08dfcf2f82bd483b42`  
		Last Modified: Tue, 04 Mar 2025 21:59:47 GMT  
		Size: 294.4 KB (294391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b704ebeab23a12c1391628665925189d800995f90d6bab09fc653f615d683c07`  
		Last Modified: Tue, 04 Mar 2025 00:32:19 GMT  
		Size: 129.8 MB (129838774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d1dac11197a77aa0b9734746f43e01f9783546b893724220b1c0553d80e2b5`  
		Last Modified: Tue, 04 Mar 2025 21:59:47 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:4986b08c392ea8daf188d775d1d33c9d8711e2046b9cb1e3ed9689d013c03466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 KB (229867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14f3112bf4d1fbef49288b2f727b86dd6ccdee675722cf87453362cf091fd876`

```dockerfile
```

-	Layers:
	-	`sha256:f09801574e792a00a606ded700fc771c1b6a851932866d270eec4d3391272209`  
		Last Modified: Tue, 04 Mar 2025 21:59:47 GMT  
		Size: 205.4 KB (205355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8afa7930af56f16cf48ca349ddfd0c81e775915f870baba97326fab99029da73`  
		Last Modified: Tue, 04 Mar 2025 21:59:47 GMT  
		Size: 24.5 KB (24512 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; arm variant v6

```console
$ docker pull golang@sha256:64da910104d861c1a2dd83b2b0fa7f3a2bfcfcc7e14a3ec654c75819f39ac0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127095484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d277df4ba61a679d911bc6cbc121944db9c7951ff24419bcac2b0367455473`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 00:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOPATH=/go
# Mon, 03 Mar 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Mar 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
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
	-	`sha256:908353bf334c8298bf4221ed4995e78c699ff58f6af7b91fa91bb0e60c060533`  
		Last Modified: Tue, 04 Mar 2025 00:32:51 GMT  
		Size: 123.4 MB (123426962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2850b38bc379c8e8cb16a3cf577c9edc896133004337eae297b507ee45c4c9c`  
		Last Modified: Tue, 04 Mar 2025 00:45:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:73e0905f77f4b03182b7e0f09b9b8d95759751dba58ff742d6c59b9ad2fcab2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e444f7f31cf1ee4cfb0ee1530e28423721267e1ffbb6291487a2c2144610fe5f`

```dockerfile
```

-	Layers:
	-	`sha256:6aaf7c5c9290fd745f97eaad1f06386dae2f325fe89f222bdb21f76809ce27bc`  
		Last Modified: Tue, 04 Mar 2025 22:00:18 GMT  
		Size: 24.4 KB (24405 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; arm variant v7

```console
$ docker pull golang@sha256:8cc95f1d1196e1b3ef49950a067448676c5bcb32737c9c5fd9fff65ed0608b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126478432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb63ec667fbdebb8e164abc612a52a0fefaf379d32a3241e21c232036df87d1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 00:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOPATH=/go
# Mon, 03 Mar 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Mar 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
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
	-	`sha256:c66a4732c96edfeab450050a70f02b158342482c6f2a5dcf7aeba30aac7fcc17`  
		Last Modified: Tue, 04 Mar 2025 00:33:46 GMT  
		Size: 123.1 MB (123087551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c8d123e04aff049ea710898b957ea9a293eb531cd3344509f37377c49bfdfa`  
		Last Modified: Tue, 04 Mar 2025 00:43:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:e0b4bf7fba1ac0b04413484d4a93aaa0466cd1dbaedb19ee7a4d05ecae89ceae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 KB (229955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e08db218e47434c4068adc66486c3e97791e7804f238e7df3d9bd770a3f9dfa`

```dockerfile
```

-	Layers:
	-	`sha256:d80db94360323547a5b8b9f16ea07ed93ba553c9ed07f32885eea9b4b530a33a`  
		Last Modified: Tue, 04 Mar 2025 22:21:06 GMT  
		Size: 205.3 KB (205335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9edeb098ba8d2323199c61d5a9d8ff74c55fe7943fa08bdfefd98fcfd934a490`  
		Last Modified: Tue, 04 Mar 2025 22:21:06 GMT  
		Size: 24.6 KB (24620 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:c50beea462f0ea98c58bf2d65409f64eafb7740bea7b00b55da4017335772381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127009360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e0254883ed90f4fa119e138e00d4d77d07fa6aff53101a473a3693e88abaef`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 00:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOPATH=/go
# Mon, 03 Mar 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Mar 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
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
	-	`sha256:d2fb2f15af0e54e78387b98706e083a5882e5cd46c9ae24a07d9c9a7de13391d`  
		Last Modified: Tue, 04 Mar 2025 00:39:29 GMT  
		Size: 122.6 MB (122620567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76e27c8c9882f3790195ea2f7a13f5dcd62768db7b3a103257ff43271df7ab1`  
		Last Modified: Tue, 04 Mar 2025 00:46:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:379e8428a0a727a4433d94d97857b8c5e0135be16df5fb582e8308861768aab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 KB (230035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8309c80f22a31f44f4b49d73cdb2649f3374e47469aa22d9fc51f2ad2b6f5d20`

```dockerfile
```

-	Layers:
	-	`sha256:c3a12fae004e47ebcad104d30808ecb4d55f48c88890e9c7b4454fbef49dda5c`  
		Last Modified: Tue, 04 Mar 2025 22:27:07 GMT  
		Size: 205.4 KB (205387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adbb31b21aa15b0fd4c18be696d01b6c8951d6d16bf8ace5943c4d8692e0ba5a`  
		Last Modified: Tue, 04 Mar 2025 22:27:06 GMT  
		Size: 24.6 KB (24648 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; 386

```console
$ docker pull golang@sha256:266f530cfbf060ed86ed4e08cc9f490732739edb2f19eadc92f80c9695acdab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.2 MB (130225192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53d5bf7ec10f2189fdf6dc1e6ba2a62a2c5d9ce98dfa677e600832cf2b4d13cd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 00:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOPATH=/go
# Mon, 03 Mar 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Mar 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b3d7db73e90671cb6b7925cc878d43a2781451bed256cf0626110f5386cdd4dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.5 MB (3471668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe669adf82b0d438a8c3c8c6e1381b912bb7d84063f6d6fe7a15279420c959cf`  
		Last Modified: Tue, 04 Mar 2025 21:59:44 GMT  
		Size: 295.1 KB (295136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc05ee2fc954345b4dc36b55c348df7ba176cd1d037dcc0fd8ba6eedfb02eea9`  
		Last Modified: Tue, 04 Mar 2025 00:32:40 GMT  
		Size: 126.5 MB (126458230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794529a2e1841947c0aa2b0a6fc2a0f2a67a1b3b2a2d12aa9ff291c3b8bfab18`  
		Last Modified: Tue, 04 Mar 2025 21:59:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:4701ae70ae8ecb9396c4dd81f4954582c494af9857d9171d1a03ae805b4e14b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 KB (229779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09e7d58f73a2f8f62db32cf79445c1830d06867a92454bd5f1962f548fc9295`

```dockerfile
```

-	Layers:
	-	`sha256:7420243ad75ee66c37852a8af53d9539c8a52d6174e36b8382ccaf97d641a319`  
		Last Modified: Tue, 04 Mar 2025 21:59:44 GMT  
		Size: 205.3 KB (205300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77f53bbc8782326390e2f7e8d9a9c9e07f599bf5d8a96de03e8110efcc4419ed`  
		Last Modified: Tue, 04 Mar 2025 21:59:44 GMT  
		Size: 24.5 KB (24479 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; ppc64le

```console
$ docker pull golang@sha256:85e3ef1a1403dad953b64018c4a29a353e6f70ef09037b0f63e9da5faa32caa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.9 MB (128867817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4607fc3fe35b8fb4f9817a0c15ae17d86ef8808274466eb020b6d9585e39f9fd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 00:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOPATH=/go
# Mon, 03 Mar 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Mar 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
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
	-	`sha256:de94f4e3ebdd3654e0bb93d6ee292377b5f63d04585b0ae2f0dcd851ba62d914`  
		Last Modified: Tue, 04 Mar 2025 00:33:04 GMT  
		Size: 125.0 MB (124994092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ecd04e1616d0c13a3d4bb51c9ac17f1e1760958e33cb83aeb460bce89468a9`  
		Last Modified: Tue, 04 Mar 2025 00:49:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:e13982bfe6b83b0a9b6354b457e4ac0d7b6c2098144a0060f3f82a8a4c7039ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 KB (228023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ab03d2962184801cc2fd39b13c6593c847b99dbd597202f788a0dff4bdcd79e`

```dockerfile
```

-	Layers:
	-	`sha256:4891a3101d7456afe46c6f00258d3dafb5f6b6a1ea1be6795c9d0cf859ae89d3`  
		Last Modified: Tue, 04 Mar 2025 22:04:42 GMT  
		Size: 203.5 KB (203466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d201024ea114397cda99f2f14b9da46671df900d361daecd65a0a7ba928b9a2`  
		Last Modified: Tue, 04 Mar 2025 22:04:41 GMT  
		Size: 24.6 KB (24557 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; riscv64

```console
$ docker pull golang@sha256:42bcd85259c85248fbd765df33b3718724362ac89593841f082587bfd2bad6b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129073294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e469c7e52339d96b7a3eafd143ff97c77e639a6b3e022d86820755193960296`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 00:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOPATH=/go
# Mon, 03 Mar 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Mar 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
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
	-	`sha256:6c633f7fa993ac4c1efa563a24885fa8695e4a2df8b8a5fd4fd881545bdcea50`  
		Last Modified: Tue, 04 Mar 2025 01:10:32 GMT  
		Size: 125.4 MB (125404458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2fa8ba5a79a3d962c758d92076f9736416bb1f232202af5db599d3cdc7052db`  
		Last Modified: Tue, 04 Mar 2025 01:47:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:6de4fb7228a0d0a0771413bc23927e5a19b7c6e6ce4b6d862a88e40791e96c5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 KB (228020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f2cc2603488f3367ece6e39a5b96902097eba259a319de7335834670d241a5`

```dockerfile
```

-	Layers:
	-	`sha256:aad5779dea9a2362c622d28772c1b4f7c00221a55e1bcc100fe9b0d8461a90a5`  
		Last Modified: Tue, 04 Mar 2025 23:12:26 GMT  
		Size: 203.5 KB (203462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b07fc72e288df4001326a7920801908c3e20e0edfe177fe7eeca13981d897185`  
		Last Modified: Tue, 04 Mar 2025 23:12:25 GMT  
		Size: 24.6 KB (24558 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; s390x

```console
$ docker pull golang@sha256:af3cbbc1a5540e8f4bf6f45203f57afff7ea2216b262c520e0890c701a9f8951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131117012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b05aea0639961141b8f9d71642c595f991d7d2fe5b1b1c010c420d2d8fcf562`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 00:23:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOPATH=/go
# Mon, 03 Mar 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Mar 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
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
	-	`sha256:1a90f174e12bc58df6074c85a9d3459219dd43fe7d642ba33065f9e29227fef9`  
		Last Modified: Tue, 04 Mar 2025 00:32:29 GMT  
		Size: 127.4 MB (127357030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e2ecb48992d10365bb0f6050eb70629dd4916a9f90f0405cc5ba46b160a01f`  
		Last Modified: Tue, 04 Mar 2025 00:44:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:aa440bdceebff7029f6b5f4f0886a44ed6c0a5bb160527dd44b5e98748250039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 KB (227916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1fb0bc39f0e2897ecbccc2998901dc90920910b270cd6a85510b3bb20827f6`

```dockerfile
```

-	Layers:
	-	`sha256:1d9f9d06ec98722b719d3ff6da2abfa48f5f1302c7a140cb816f87bec16709d3`  
		Last Modified: Tue, 04 Mar 2025 22:03:01 GMT  
		Size: 203.4 KB (203404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82fedf8317faeb9dfa9472b2e25fff854baf8344a679fd151472c374980155ec`  
		Last Modified: Tue, 04 Mar 2025 22:03:01 GMT  
		Size: 24.5 KB (24512 bytes)  
		MIME: application/vnd.in-toto+json
