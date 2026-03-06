## `golang:1-alpine3.23`

```console
$ docker pull golang@sha256:2389ebfa5b7f43eeafbd6be0c3700cc46690ef842ad962f6c5bd6be49ed82039
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

### `golang:1-alpine3.23` - linux; amd64

```console
$ docker pull golang@sha256:d337ecb3075f0ec76d81652b3fa52af47c3eba6c8ba9f93b835752df7ce62946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71374932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e951cd8dd18b7c05b5a943b21e5f1a3e7088422c21a9c4c8658dd183ee3b636d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 01:11:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 01:12:05 GMT
ENV GOLANG_VERSION=1.26.1
# Fri, 06 Mar 2026 01:12:05 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 01:12:05 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 01:12:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 01:12:05 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 01:12:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 01:12:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644a983862e3898a5575fef5c81590cbc92d1c1e1bf5f61112c0cd35e6b7be98`  
		Last Modified: Fri, 06 Mar 2026 01:12:20 GMT  
		Size: 296.1 KB (296074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbff1d4eb7eece408734c05c8c63a49bb181871bc1280cff3f0e28d25a4ea28`  
		Last Modified: Fri, 06 Mar 2026 01:12:19 GMT  
		Size: 67.2 MB (67216879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ee208a3600503f47e9ec1ced0e8abb825a045473b092f1fe872b81d9873706`  
		Last Modified: Fri, 06 Mar 2026 01:12:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:e3c595f9d75c6a15d44a52d77083e45f188a1db43d6ff571f3394c4e9383ac9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.1 KB (223050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f29caed203563c226a66b6d65564a225cbe3c1d70e87d0a510dcf0bf83786a`

```dockerfile
```

-	Layers:
	-	`sha256:391498a63c0e75a22fadbb6a6bdb209527a0de14c316e7de2a8fb2820ba6141e`  
		Last Modified: Fri, 06 Mar 2026 01:12:21 GMT  
		Size: 197.0 KB (197023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaf43e45e2d1ac5fd2a878ac5c690bd8a36f7d2b70a89f8bff6d8114e2afd385`  
		Last Modified: Fri, 06 Mar 2026 01:12:20 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.23` - linux; arm variant v6

```console
$ docker pull golang@sha256:67b44516a1a8ef414d0ddd09f716437fc8cdb6f90eb7b664c3d7792b2a475fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69624382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e84acb9c797013b83501acbc9a8f4f2eb66bb1c5086639ef19ba83d464fb962a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 01:12:48 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 01:13:12 GMT
ENV GOLANG_VERSION=1.26.1
# Fri, 06 Mar 2026 01:13:12 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 01:13:12 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 01:13:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 01:13:12 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 01:13:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 01:13:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1109a5071b02b1044612a78906bb866947d31adddc34582210c9b1df0d6c2d`  
		Last Modified: Fri, 06 Mar 2026 01:13:26 GMT  
		Size: 297.3 KB (297262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96dfc026f620d0674c1a89536cf39d64e74602dba70d199d21c90c7b01bd9ba2`  
		Last Modified: Fri, 06 Mar 2026 01:13:28 GMT  
		Size: 65.8 MB (65757141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bf8dd9810462b9c3cf1794258fb5fb3448a3b8ff5e6eee0b1449b61acbdab2`  
		Last Modified: Fri, 06 Mar 2026 01:13:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:d54c761d6bcae0dfddfd854f484e1dd74b27a1150475e5f424641f29441735e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a21d6a36c406e30cb27cdf7dc0e2521f3b2615324c7d90dca44153aac961cb4`

```dockerfile
```

-	Layers:
	-	`sha256:7e01ace3e1c231046a4743f2afe8bc2dd5b8b41d12234193503b11c3671a8cb9`  
		Last Modified: Fri, 06 Mar 2026 01:13:27 GMT  
		Size: 25.9 KB (25950 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.23` - linux; arm variant v7

```console
$ docker pull golang@sha256:c2cadd977d3a1ddeaff3b8b56200033cbdebf444a759137989db746fda5da3a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69335189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d49c76c237ff036b72d840e7a0baee8dadbee6e75be7e602099e8c197b2f1c6f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 01:11:40 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 01:11:52 GMT
ENV GOLANG_VERSION=1.26.1
# Fri, 06 Mar 2026 01:11:52 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 01:11:52 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 01:11:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 01:11:52 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 01:11:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 01:11:55 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8528f8fd0be7185e5fdd156634e845361ee385919d5f74f4dcdcdb37ceb8ff5`  
		Last Modified: Fri, 06 Mar 2026 01:12:09 GMT  
		Size: 296.2 KB (296202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c71a08a325c7d5f7b73bc8da93a0980d5401206ec7c3b40584ca8d21ca82f77`  
		Last Modified: Fri, 06 Mar 2026 01:11:53 GMT  
		Size: 65.8 MB (65757104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffb5ff6c2a264c2b3f1d07eb347799ecf4b393d1b4bfabb7c4d26a87c7354ae`  
		Last Modified: Fri, 06 Mar 2026 01:12:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:2b5cf5324b0bc8af9220873e8a4e89856f33b279153cb618f21127f3e6756767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.6 KB (222589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfba8c09a387059639844828f1c214b4c2af92612f311e74f5053511acf4641a`

```dockerfile
```

-	Layers:
	-	`sha256:87d590546d55a8a46e716334c68d2cd37f44297a8fa7803c815cf94614eb80a1`  
		Last Modified: Fri, 06 Mar 2026 01:12:09 GMT  
		Size: 196.4 KB (196425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba985584bbd18a26b8585f77b7096664c2953e8a82edae83441550a95fdd9fad`  
		Last Modified: Fri, 06 Mar 2026 01:12:09 GMT  
		Size: 26.2 KB (26164 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:c500d8fac0707aa2a887d7e426530cfef09549c9c87ac0c2998543a89ce89d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68602227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e21b717a70267b4dffa2ef112863535d2265973f80649d69ce41ab3e407fd3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 01:11:35 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 01:11:46 GMT
ENV GOLANG_VERSION=1.26.1
# Fri, 06 Mar 2026 01:11:46 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 01:11:46 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 01:11:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 01:11:46 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 01:11:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 01:11:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62764d53541d11f63129956ccd8b52d20597aca289f431759deb77ea2275f569`  
		Last Modified: Fri, 06 Mar 2026 01:12:03 GMT  
		Size: 298.8 KB (298849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49db9bb2f958b7444a4f28145af7a815dd0a47fec1608d03e2f1c673b3aa858b`  
		Last Modified: Fri, 06 Mar 2026 01:12:04 GMT  
		Size: 64.1 MB (64106129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4901bef231fb8a6d26e9c2ceb808c5c0ed8319bb7a5f6b5a284cac28d8f72b8e`  
		Last Modified: Fri, 06 Mar 2026 01:12:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:48c6be66d5da08e26dd28ae8247278a3cb68e45d5376528fb12157bad3f614a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.7 KB (222686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5bb3d7b3196b6da4412d404cfd3ea26145bce11bff932617a38f3aba1f1670b`

```dockerfile
```

-	Layers:
	-	`sha256:74086c020c3bb3b28ed3149505431fd4c6efefdd60545dfa971b8f07bd912284`  
		Last Modified: Fri, 06 Mar 2026 01:12:03 GMT  
		Size: 196.5 KB (196477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ef3f3aabd7a3e1251b487338c7b2d51a5cb6e43148892b97f55c7175d89d2a7`  
		Last Modified: Fri, 06 Mar 2026 01:12:02 GMT  
		Size: 26.2 KB (26209 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.23` - linux; 386

```console
$ docker pull golang@sha256:c8fe9eb001d3a0ae74c71fc47fa9c2e4b4fb455b6cffeb3623ff756549f237ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69525613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4504c97d0f9128a8ab181d31c16c53bd6a6657fb71d895d120ae48f3c4d8c14`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 01:11:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 01:12:10 GMT
ENV GOLANG_VERSION=1.26.1
# Fri, 06 Mar 2026 01:12:10 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 01:12:10 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 01:12:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 01:12:10 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 01:12:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 01:12:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a0a043a2110e664eabec901c2a78ff9d0e376bd291a539dcb6606ba461f42e`  
		Last Modified: Fri, 06 Mar 2026 01:12:25 GMT  
		Size: 296.7 KB (296661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb07caf9c739767295e4b0d3b36abebfa29f9d22222644122dcb4a2deeeddd8`  
		Last Modified: Fri, 06 Mar 2026 01:12:15 GMT  
		Size: 65.5 MB (65541795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80c4ce14611ccc642ebabb791f7ba04ac4996dfb0cb5067fb5ade575104cc6c`  
		Last Modified: Fri, 06 Mar 2026 01:12:25 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:d08750b2b8f4df3e8c2eb1a6ddfc569a1c87e90ba11fe6862828ab1c5006ba41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 KB (222932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a5d3b5ef59d9f9b7d1cbbd900fb8c1cacfbc480f8d5ebb284f8754668092118`

```dockerfile
```

-	Layers:
	-	`sha256:d3449c180bef88f2a494ac553db228d0b9ea24ce18d938408b04bd572ff860e9`  
		Last Modified: Fri, 06 Mar 2026 01:12:25 GMT  
		Size: 197.0 KB (196962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acc963059f6cf4134522dce5ce2d0c7b9d0dab0390e5b4708ea3bcea66227a80`  
		Last Modified: Fri, 06 Mar 2026 01:12:25 GMT  
		Size: 26.0 KB (25970 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.23` - linux; ppc64le

```console
$ docker pull golang@sha256:9599a28721e53521c9581402cb1747b92aba27eec05a22e0d8bb9ac061f7037e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68895047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0d4f2f8110be9e380485988344344a9ddd258874b5a33cd11dbe2658bd3362`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 01:12:22 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 01:10:37 GMT
ENV GOLANG_VERSION=1.26.1
# Fri, 06 Mar 2026 01:10:37 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 01:10:37 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 01:10:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 01:10:37 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 01:12:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 01:12:41 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e662a4a3a7cbf153b23a38a961b2078122cec8354bbb9cc27381fb9fd6abd628`  
		Last Modified: Fri, 06 Mar 2026 01:12:55 GMT  
		Size: 299.3 KB (299266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace710cfb3bb4da72d185d83d05e86cb22a686c0abd5be3e83cdf74e34b68d02`  
		Last Modified: Fri, 06 Mar 2026 01:12:05 GMT  
		Size: 64.8 MB (64765980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3645e9a27139f1a82b884568a2ebeca4b84caad36f011c206583bab85d758e73`  
		Last Modified: Fri, 06 Mar 2026 01:12:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:8de185a402ea6fdada7e6e2b17889d4756a3ceff5fc892df95c66f18b2ab81f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.5 KB (222544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75dc99784aaef515716b4bf4000b6229947931fd8311b42f7f95463bcf947590`

```dockerfile
```

-	Layers:
	-	`sha256:c084b6002352ab6503729660c496675683d24a47cbaae1b7e077d702b3531424`  
		Last Modified: Fri, 06 Mar 2026 01:12:55 GMT  
		Size: 196.4 KB (196446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8f3393cca317c5136563fa232393c66aad9b47d2ff4851d4cdf9f1684133cb2`  
		Last Modified: Fri, 06 Mar 2026 01:12:55 GMT  
		Size: 26.1 KB (26098 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.23` - linux; riscv64

```console
$ docker pull golang@sha256:e85ca91d33beab799c912868930d57d46abeb6ad13a4f9a42268c8ce89296218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68959455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f70336439e35d3d28411e6f0fbbd95fecbbf8c8d603ebe4861294014081234a1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:12:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 01:12:00 GMT
ENV GOLANG_VERSION=1.26.1
# Fri, 06 Mar 2026 01:12:00 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 01:12:00 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 01:12:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 01:12:00 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 01:20:33 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 01:20:33 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f6a28a44ff91c18ab295ffef6822bbaccafe002bd1f4a117c179d363e86328`  
		Last Modified: Thu, 29 Jan 2026 19:14:45 GMT  
		Size: 296.5 KB (296505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7741c0adede1d2e9597a871420fa82f196151039c468eac7755d531cfe50922`  
		Last Modified: Fri, 06 Mar 2026 01:18:47 GMT  
		Size: 65.1 MB (65077505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15647ffd280dd6c01380ff7053031d8b9c620450567c4be60c59090f35528445`  
		Last Modified: Fri, 06 Mar 2026 01:21:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:31f7e7f4f2c0f335298de8ce75ea7abcd85c16470e6f85638408dc995f6164d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.5 KB (222541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a2206b8eb3ea2e02299a4fed61f9120b1a8e13fbb9b6177fc47ea2ccfeacf1`

```dockerfile
```

-	Layers:
	-	`sha256:3481c7b4d85afb6b5143502c3395c31f74c2e67ed4520e918b9989a398128949`  
		Last Modified: Fri, 06 Mar 2026 01:21:40 GMT  
		Size: 196.4 KB (196442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6473deb0895bad651c5e99f0629a19c572fb3a7cb619732cf115f6940422a16`  
		Last Modified: Fri, 06 Mar 2026 01:21:40 GMT  
		Size: 26.1 KB (26099 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.23` - linux; s390x

```console
$ docker pull golang@sha256:0e7b01909f281aadf4a15e54924604af694b7d2eb11d6ca713acd5a236cacffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70455421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b10eeb482e0235eac8987716ae3ee34d07f82f29643952ed1e7f94be8eed5d0e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 01:10:35 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 01:10:52 GMT
ENV GOLANG_VERSION=1.26.1
# Fri, 06 Mar 2026 01:10:52 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 01:10:52 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 01:10:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 01:10:52 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 01:10:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 01:10:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79449d8f37ca627569c53e700d0b5ae9b25ebeef0a08dac074cc719821e22ba7`  
		Last Modified: Fri, 06 Mar 2026 01:11:18 GMT  
		Size: 297.2 KB (297183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ac4fc296175935efd55931d7d181f8e7c85d38405c6fdcb1a96bcb9115d7eb`  
		Last Modified: Fri, 06 Mar 2026 01:11:11 GMT  
		Size: 66.4 MB (66432747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d729dd9fe0b725e8d914a70685a29638ee35da82ebe402e075a4ca4768e879b3`  
		Last Modified: Fri, 06 Mar 2026 01:11:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:e3be9084be223a425040fab9c3401a991d7d24d2ffb4a4060ccbd0ceb6187255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.2 KB (222226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578912929b2ae25a4c8aa6e901d7715d1c1fbd94ad0585dcef9abb05d55ee176`

```dockerfile
```

-	Layers:
	-	`sha256:0b59799ab5c85850065347b8ff60a0fa8545a27594ca004324df99bb4efafe50`  
		Last Modified: Fri, 06 Mar 2026 01:11:18 GMT  
		Size: 196.4 KB (196372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25690efef2b83ad725d3df5bc0a87160b9b3d9a4503eb870208f67a40e336fc8`  
		Last Modified: Fri, 06 Mar 2026 01:11:18 GMT  
		Size: 25.9 KB (25854 bytes)  
		MIME: application/vnd.in-toto+json
