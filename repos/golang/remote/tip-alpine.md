## `golang:tip-alpine`

```console
$ docker pull golang@sha256:d0feeb965c9e5fceca9abb8c57c23832aac0ec40dcaf31e3c08034f1ff6b512c
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

### `golang:tip-alpine` - linux; amd64

```console
$ docker pull golang@sha256:b3d84beabd181896ee8d9fabe9e1720ff1c2476c3ffd84721a205381d6ee8bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.2 MB (106209524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82782977e8cb0d2722fdee0547cd6e11b648160bec92b53e77bd7321451a4ac`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:31 GMT
ADD alpine-minirootfs-3.24.0-x86_64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:31 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:57:35 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 10 Jun 2026 20:59:33 GMT
ENV GOTOOLCHAIN=local
# Wed, 10 Jun 2026 20:59:33 GMT
ENV GOPATH=/go
# Wed, 10 Jun 2026 20:59:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 20:59:33 GMT
COPY /target/ / # buildkit
# Wed, 10 Jun 2026 20:59:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 10 Jun 2026 20:59:36 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9b70e313681f44d32991ec943f89228bc91d7431d4a84feafc269a76e3f96a63`  
		Last Modified: Tue, 09 Jun 2026 20:11:36 GMT  
		Size: 3.9 MB (3866755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac846c9f177a3fbf74ade075971e4141d0c61c17ee5a78f5f0d82913a1820ed3`  
		Last Modified: Wed, 10 Jun 2026 20:59:49 GMT  
		Size: 290.2 KB (290241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9caf2b5917603f564e8b31c080871596acbc699caf5fd0fec4940c836746ec3`  
		Last Modified: Mon, 08 Jun 2026 22:46:13 GMT  
		Size: 102.1 MB (102052370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a622546e16ca7e4b0baf13c45da22445de8a02533e27be9c661434f6a887ef`  
		Last Modified: Wed, 10 Jun 2026 20:59:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:7863bbdca26ffc779e7638546dc24bb222958a737b72be702597dbfbb93380d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2965f8dcee17cdaf6c4d18246cbf49dd32dc3c758710561effba067a952db6c`

```dockerfile
```

-	Layers:
	-	`sha256:7e4360efd5a6e0145dcb8fbe9fccda268af159660d3dbf1557ac58c5c512c035`  
		Last Modified: Wed, 10 Jun 2026 20:59:49 GMT  
		Size: 193.6 KB (193644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb7cc2799bae191ccb0c40a97c53b72a62cb3800f019f86fc73025e619101c13`  
		Last Modified: Wed, 10 Jun 2026 20:59:49 GMT  
		Size: 25.1 KB (25099 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:f8b2299e1a7b7a7a379f46bc2c5c6170e7a0421cddebc0b01ce59a19a658725a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101916871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7072fb23f538530b3e84d79899874609b4a2fde38897b35464fd0f440bb5a8d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:25 GMT
ADD alpine-minirootfs-3.24.0-armhf.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:25 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:54:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 10 Jun 2026 21:39:31 GMT
ENV GOTOOLCHAIN=local
# Wed, 10 Jun 2026 21:39:31 GMT
ENV GOPATH=/go
# Wed, 10 Jun 2026 21:39:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 21:39:31 GMT
COPY /target/ / # buildkit
# Wed, 10 Jun 2026 21:39:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 10 Jun 2026 21:39:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d44d12cd5c9ecc8e4b75201d67412f77b79157eaffaaed75c3b717bcd42f61e1`  
		Last Modified: Tue, 09 Jun 2026 20:11:29 GMT  
		Size: 3.6 MB (3575314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ab3c361631b5bfa3132c0c2adbea6b5c3e9e57a6b79b435419d53ebb9621da`  
		Last Modified: Wed, 10 Jun 2026 20:54:55 GMT  
		Size: 291.0 KB (291031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04993cb4ea53eb54b934632859a46a3fda346d78f94e5c8c7587a367646e0cf1`  
		Last Modified: Mon, 08 Jun 2026 22:47:15 GMT  
		Size: 98.1 MB (98050368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ed8014d4e33594d07922edb0920d36bebfd53f6de9925af5a358fe9d60ceac`  
		Last Modified: Wed, 10 Jun 2026 21:39:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:4ead2d03c0b3b96030035b036be19ba928c8781612250f37f953f40dd64bebb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea72df30160a827a1a963b6e0496fe08cabe473e3f7a68ca003fa9f4bd23f4b6`

```dockerfile
```

-	Layers:
	-	`sha256:27be2918563042c12d4a6328c3dfd761e71239400c3674712dcac18a823bf39b`  
		Last Modified: Wed, 10 Jun 2026 21:39:46 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:fa5b989cda7a54406eac08d2f029826e8eec9a1b32b37f625c6fa20ad1623053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101311545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510289963e333cab8cf7abe06bf3ef23bf2ca2cf0085d7ac2cebd3cf151c073f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Jun 2026 20:14:38 GMT
ADD alpine-minirootfs-3.24.0-armv7.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:14:38 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 21:36:14 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 10 Jun 2026 21:39:25 GMT
ENV GOTOOLCHAIN=local
# Wed, 10 Jun 2026 21:39:25 GMT
ENV GOPATH=/go
# Wed, 10 Jun 2026 21:39:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 21:39:25 GMT
COPY /target/ / # buildkit
# Wed, 10 Jun 2026 21:39:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 10 Jun 2026 21:39:28 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bce674d5697a824549061f4985dfd06a60c018b96ba50b18b7bc1f9ad6143570`  
		Last Modified: Tue, 09 Jun 2026 20:14:43 GMT  
		Size: 3.3 MB (3286160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381b6bf6b1af4a14ba68d4863cb9c3c2a3e7b487c2e6461ec347569e5ac68d17`  
		Last Modified: Wed, 10 Jun 2026 21:39:43 GMT  
		Size: 290.2 KB (290192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6017a74f67fe3bf0e9dc5d0c334ab5929b4a454a86c2f391ecc6e1d3f6697e53`  
		Last Modified: Mon, 08 Jun 2026 22:48:21 GMT  
		Size: 97.7 MB (97735035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2674749c29020e9bab8d11e31cbd64560ec251cb04ed256b72587e6d2fe06d`  
		Last Modified: Wed, 10 Jun 2026 21:39:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:d90778ce452eae4d2873d4e40316e493dca14a96f088d19d96c985ad3020a232
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 KB (218236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fced00a3ef91bb7442e49bfa750a03d1263bf25e8522c37df61bdfec4a3e2765`

```dockerfile
```

-	Layers:
	-	`sha256:ed0cfd116e83fc814eeaf14ea852d024c72ee6b1b640027b91346ca4f70f809d`  
		Last Modified: Wed, 10 Jun 2026 21:39:43 GMT  
		Size: 193.0 KB (193014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a899508ab45d2c7e0c9c163c9593fe61c89889f8af1bc911f1c03a79ba3814fa`  
		Last Modified: Wed, 10 Jun 2026 21:39:43 GMT  
		Size: 25.2 KB (25222 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:f234456e26555e6a967a12bfd0cabb2db0ca5c5c8e157f504ca3265e60147537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (100964764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a15a92835da615445f538f41086b402597783b649607ebb8814e47cb7f0a54f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:09 GMT
ADD alpine-minirootfs-3.24.0-aarch64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:09 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 21:01:02 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 10 Jun 2026 21:03:05 GMT
ENV GOTOOLCHAIN=local
# Wed, 10 Jun 2026 21:03:05 GMT
ENV GOPATH=/go
# Wed, 10 Jun 2026 21:03:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 21:03:05 GMT
COPY /target/ / # buildkit
# Wed, 10 Jun 2026 21:03:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 10 Jun 2026 21:03:08 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c05efffaed614b5ff4e3b9a80136e7c0eed0b47f434802c81baf254c0defca91`  
		Last Modified: Tue, 09 Jun 2026 20:11:14 GMT  
		Size: 4.2 MB (4202330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351bf5de6bfe5dfe243e21540af8fb125b15004db4e28e05fa2aa754d08322ed`  
		Last Modified: Wed, 10 Jun 2026 21:03:22 GMT  
		Size: 292.9 KB (292859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2308f1cb629a8c8fe52b3b591bdcfb51ba3716d584492ccac8858ffd19fbe4d4`  
		Last Modified: Mon, 08 Jun 2026 22:46:27 GMT  
		Size: 96.5 MB (96469417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3714a148d8c27cd50033bd6830f32f63347a20de31b319d16063686a63e03e`  
		Last Modified: Wed, 10 Jun 2026 21:03:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:5e5191e7419bf96266507e05702888b99f82b13ff93852e0aba8c4b5d46df55e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 KB (218304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91dc3c34937da544cf9f331d227d7e36fd3c3d396a3a04bf971fff3b21148582`

```dockerfile
```

-	Layers:
	-	`sha256:db2e822c083fa59746e6d2b836fe9cecbe52b204950b584a983d3ad69d47684e`  
		Last Modified: Wed, 10 Jun 2026 21:03:22 GMT  
		Size: 193.1 KB (193050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11f5c2b9070a9a77892911d2f0fc6a23fef3b70dbf06423c33b003d8100d8d2e`  
		Last Modified: Wed, 10 Jun 2026 21:03:23 GMT  
		Size: 25.3 KB (25254 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; 386

```console
$ docker pull golang@sha256:e0e5c5a62d92f639a13986e404e73814c13721f1a2f41f72f09b078993a5c6e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.8 MB (103760552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb0b037e0a018c61a85d5e0584e62deef9726b232bf248f5fb32beeeae91a75`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Jun 2026 20:10:54 GMT
ADD alpine-minirootfs-3.24.0-x86.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:10:54 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 23:12:08 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 10 Jun 2026 23:14:34 GMT
ENV GOTOOLCHAIN=local
# Wed, 10 Jun 2026 23:14:34 GMT
ENV GOPATH=/go
# Wed, 10 Jun 2026 23:14:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 23:14:34 GMT
COPY /target/ / # buildkit
# Wed, 10 Jun 2026 23:14:37 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 10 Jun 2026 23:14:37 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:14b4480cdb6be1a40aafc14c9089d92843794d03fc3115b849ddc49717c25982`  
		Last Modified: Tue, 09 Jun 2026 20:10:59 GMT  
		Size: 3.7 MB (3691754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ce623cfbac093c447ff61a895000aca141e035f9c8dc167bf9156e423fd6e5`  
		Last Modified: Wed, 10 Jun 2026 23:14:51 GMT  
		Size: 290.6 KB (290630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c856874e83d87ce8611744942560effd5d1e879f3a49a6259f9e0f789a54f9b`  
		Last Modified: Mon, 08 Jun 2026 22:47:42 GMT  
		Size: 99.8 MB (99778009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2c4308bf9492124a169e6d0007254a8eacbfdf66d49de355303e5c0a5fb89c`  
		Last Modified: Wed, 10 Jun 2026 23:14:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:62a109ad06eb1bff1919cbada32e415de8f4ab56b37418539e34c9dcee6ab910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed33bcdd858990e2bc351b703521dd1636e11e66bee2d0a8734a487b421b2b5`

```dockerfile
```

-	Layers:
	-	`sha256:da5f645ae31271e0fdbade434b13a6d926576d403865674fdbc942771a0d0d53`  
		Last Modified: Wed, 10 Jun 2026 23:14:51 GMT  
		Size: 193.6 KB (193603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:086ceadcaa72da691a445680b9e850c1d037d4b8c29e1d79d1ed1c5ba17a3ff8`  
		Last Modified: Wed, 10 Jun 2026 23:14:52 GMT  
		Size: 25.1 KB (25051 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:b41247e2cf0d794349b304979fe263a7dcfc97ecb76899b36cf01c329e512ce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.6 MB (102551747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69810f59a5538a9a2faf72e698f33032c19b615274f24ada6bb0a83d0339f8dc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 16:47:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 08 Jun 2026 23:06:07 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Jun 2026 23:06:07 GMT
ENV GOPATH=/go
# Mon, 08 Jun 2026 23:06:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 23:06:07 GMT
COPY /target/ / # buildkit
# Mon, 08 Jun 2026 23:11:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Jun 2026 23:11:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dfc45c5906cb105fa1bde6a534e8e48deced0c4556f99056c2f76204caa5c2`  
		Last Modified: Tue, 02 Jun 2026 16:47:39 GMT  
		Size: 293.4 KB (293393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1d5d0b8da3315c28f7e047d6d8c920d4423531520a738d9dbd717fd24afb93`  
		Last Modified: Mon, 08 Jun 2026 23:07:16 GMT  
		Size: 98.4 MB (98427267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64ee496197eb7593e189e9c4859af7ef400caff8a3bed29000144ca8e0e2d54`  
		Last Modified: Mon, 08 Jun 2026 23:11:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:79dc8eaee496eede5550a1faf2ae2c0d9c87c8ecd774ea7dfc6c98641bbbd6bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.0 KB (218027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f699b17afffa55bd6948454058f4d827a2ef3b8a4dff83df9915c12bf8f3ca5`

```dockerfile
```

-	Layers:
	-	`sha256:64b12a550486ffc62ecb7e1369eb4eebc6b13953e02c1f394fe118bfdaa707a1`  
		Last Modified: Mon, 08 Jun 2026 23:11:47 GMT  
		Size: 193.0 KB (193047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dac4d922478f5f9f8ed9541f7c81b638331e1a4a58d42f7e80db0284be23101`  
		Last Modified: Mon, 08 Jun 2026 23:11:47 GMT  
		Size: 25.0 KB (24980 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:404f810c133b06155ec6ce95de59565d3dc11a007d77738e49fa405d312bc075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.2 MB (103225559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beaaaa576c035fe100effb16af051633c50ede2fcacc8ad75ed559735dc606f4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 16:18:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 09 Jun 2026 06:45:18 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jun 2026 06:45:18 GMT
ENV GOPATH=/go
# Tue, 09 Jun 2026 06:45:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 06:45:18 GMT
COPY /target/ / # buildkit
# Tue, 09 Jun 2026 07:34:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 09 Jun 2026 07:34:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3257359d78e33ee12c186b4248dac6627cb8e26d6fd747ad8f46ed2b4fb8e1`  
		Last Modified: Thu, 16 Apr 2026 16:19:53 GMT  
		Size: 290.6 KB (290553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5a55eb95001de7bce5a945456836deb24c4f6ef91e17b9ea69478ba20a16a6`  
		Last Modified: Tue, 09 Jun 2026 06:52:30 GMT  
		Size: 99.3 MB (99347186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c23c073a607d8c2239945fff6f9fac6bab2c41f05a801c1a33e71a8a21457e5`  
		Last Modified: Tue, 09 Jun 2026 07:35:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:457d58aaab712843470fecdb2bf63db1d0beccdf6275e03a6440ef0c56bd6e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 KB (218196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218b23ea318df3bac8e592f0a8e7fb377a09465de6b751ab1ab4b10bdd7ab75f`

```dockerfile
```

-	Layers:
	-	`sha256:aadd954dc619a0ce069d40da074b59f03ec3439cb5e7af74148995b6e15d72fe`  
		Last Modified: Tue, 09 Jun 2026 07:35:20 GMT  
		Size: 193.0 KB (193043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e46abe2c38f91d401f6892f8d17570a82c0e027245ce37744c5d9a398854b14`  
		Last Modified: Tue, 09 Jun 2026 07:35:20 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; s390x

```console
$ docker pull golang@sha256:926cf992c2440d1ddd904c261dc2feaf81e6b83c4db44e4b9e7f040e06e7deb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104512765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a34b3e8fa7dc99950d02418df1b96eedfbd8d78ba76422ef31c6d394b0927811`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Jun 2026 20:18:16 GMT
ADD alpine-minirootfs-3.24.0-s390x.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:18:16 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 21:15:33 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 08 Jun 2026 22:52:26 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Jun 2026 22:52:26 GMT
ENV GOPATH=/go
# Mon, 08 Jun 2026 22:52:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 22:52:26 GMT
COPY /target/ / # buildkit
# Wed, 10 Jun 2026 23:25:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 10 Jun 2026 23:25:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4c421b7ac5771added0d41fbc2e1c815472072561366ed82ab9e16b926cb03c6`  
		Last Modified: Tue, 09 Jun 2026 20:18:26 GMT  
		Size: 3.7 MB (3730217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d256eeeff8f46fa402c1b4ba0fbc5d098f464a869c1f682188d603d41aff3038`  
		Last Modified: Wed, 10 Jun 2026 21:15:57 GMT  
		Size: 291.2 KB (291158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56217687aa3cc648280b9c7052cd68f26077339d92dab45c68b721ed5388981`  
		Last Modified: Mon, 08 Jun 2026 22:53:02 GMT  
		Size: 100.5 MB (100491232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6177c3f8fe81a7d57eea23823a90baaa3c8eb3520160c37a7c632a9d2c6b9`  
		Last Modified: Wed, 10 Jun 2026 23:25:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:8437039d16021eec59e5efb2f53c8ba2fd6606c2550ef3a3183d4fbd352e8c93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 KB (218840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a67cdeb49e24a230192022927c4d2b341d13ac59f2fd25d0872cbdc5330c62b`

```dockerfile
```

-	Layers:
	-	`sha256:03c5fb6ca7e56833a9bd6a418cbacbcfe6dde6ed6b53671275e3347b839e3389`  
		Last Modified: Wed, 10 Jun 2026 23:25:23 GMT  
		Size: 193.7 KB (193741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60113953930095774589e680d824adab1b28efb0cebf12ff5d1a658144b21cb2`  
		Last Modified: Wed, 10 Jun 2026 23:25:23 GMT  
		Size: 25.1 KB (25099 bytes)  
		MIME: application/vnd.in-toto+json
