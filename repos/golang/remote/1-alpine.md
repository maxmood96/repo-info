## `golang:1-alpine`

```console
$ docker pull golang@sha256:8274bcfe89f5989777cb759302a7ced08c8a712c81982ca3ecc9fce0626592f1
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

### `golang:1-alpine` - linux; amd64

```console
$ docker pull golang@sha256:e53336d0036c9ec9ece420d5a4cdbbfab3cf1605a8f10f4f4e057f29ce08f02a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73261972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda4b4e3db8084eaaca98ce1ca417fd27b0a35f53e7b15bff939bc646267963`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 13 Jun 2024 20:46:13 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 13 Jun 2024 20:46:13 GMT
CMD ["/bin/sh"]
# Thu, 13 Jun 2024 20:46:13 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOLANG_VERSION=1.22.4
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOPATH=/go
# Thu, 13 Jun 2024 20:46:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 20:46:13 GMT
COPY /target/ / # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7728242c92e74edf5cfd2c7e300edc2756a81630e514f71f9330869e86280f0e`  
		Last Modified: Thu, 20 Jun 2024 20:54:50 GMT  
		Size: 292.4 KB (292423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060aaf7efd0676cdf56165fe26e63a047d7f3c483ab1043d530db9370e6c28e7`  
		Last Modified: Fri, 14 Jun 2024 17:54:07 GMT  
		Size: 69.3 MB (69345548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f8e900f733a3e177aeba423378acb3315424c72b4d86836a7e71a7a1a4393a`  
		Last Modified: Thu, 20 Jun 2024 20:54:50 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:eb757b3e1b1612fedcefcc34f0ca8b7e9772eb7a55cd6cd2f084b86809a9438d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:948526f9a4ba393de7efb7ad3a652ad098ad892c35cd841603e3059cd0ed9879`

```dockerfile
```

-	Layers:
	-	`sha256:3654ca6bef71a67e26d62712315e57beab65bacc7de59ff2061c58ffddb68d7e`  
		Last Modified: Thu, 20 Jun 2024 20:54:51 GMT  
		Size: 25.6 KB (25624 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:dcc11b8cc70ef07dac6273dc695fcb3ab6e46da300ab939708f5ad1be4bd53d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71374212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae51de63cd1eed172ccfbf3b0617e64e41ac77842f79618b49518c0442c96685`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 13 Jun 2024 20:46:13 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 13 Jun 2024 20:46:13 GMT
CMD ["/bin/sh"]
# Thu, 13 Jun 2024 20:46:13 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOLANG_VERSION=1.22.4
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOPATH=/go
# Thu, 13 Jun 2024 20:46:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 20:46:13 GMT
COPY /target/ / # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb26f139748033dd9f410aaee2fa9f225bf8b64a17b5e3f1adf1ef26427ce27e`  
		Last Modified: Fri, 21 Jun 2024 03:29:57 GMT  
		Size: 293.6 KB (293605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743e448a2b4bba38b1783fb849b3f5093e7931cf69d898520c4f1462ad93a836`  
		Last Modified: Fri, 14 Jun 2024 20:04:04 GMT  
		Size: 67.7 MB (67713294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17aa4a6c18860c6004fb2b335568db1f1bcfcd78962c48ca4fe9172dda6d304`  
		Last Modified: Fri, 21 Jun 2024 03:29:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:a4f85a735cc121bc0551e7f3c586bdd882c505c38b69adaafe5c9c3f382498e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 KB (25752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28729bb70a04eebfa64f1a54511c5d076044a85e2ded716d80bfbc293b880010`

```dockerfile
```

-	Layers:
	-	`sha256:5ba9548a56652e9ca9296a0e0a640887ef0e3bf5236aab72694276b48cbd905b`  
		Last Modified: Fri, 21 Jun 2024 03:29:57 GMT  
		Size: 25.8 KB (25752 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:317a054de9f59fe8c1efd2b2274ede4ce3677a1681be94fe3ece84938bc59e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71100888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a94d2f5787117b7b42e4e97114488028584d7ec79c2ddc798bd0e869d2dc80f2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 13 Jun 2024 20:46:13 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 13 Jun 2024 20:46:13 GMT
CMD ["/bin/sh"]
# Thu, 13 Jun 2024 20:46:13 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOLANG_VERSION=1.22.4
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOPATH=/go
# Thu, 13 Jun 2024 20:46:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 20:46:13 GMT
COPY /target/ / # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc4b91d7452250ed1597b3c0ff80be71a34634d82b036162d70ec2cab221a87`  
		Last Modified: Fri, 21 Jun 2024 03:29:32 GMT  
		Size: 292.5 KB (292465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8d8376f429e08832ffbb91ed771b1b953556865415b4e4c37033a89a2f8aca`  
		Last Modified: Fri, 14 Jun 2024 17:54:08 GMT  
		Size: 67.7 MB (67713411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf50fd4501ccc7e2735edcd4a4f5bf90bb444e27ed9ee37ee24250240338ed9`  
		Last Modified: Fri, 21 Jun 2024 03:29:32 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:34d0bab019d86fb90a3a99fc42cd254dc233c0d80a41cddf7835cb11e5c83b00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 KB (25750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e42ccdfc51155279bbb1b8e6b9b4caca34688ecfc15a0bc33497f115d6b48be`

```dockerfile
```

-	Layers:
	-	`sha256:16de63f85cc4a8b49baa3d066a44c78175d824a48583e4fde0cc3f80b3b1c0e3`  
		Last Modified: Fri, 21 Jun 2024 03:29:32 GMT  
		Size: 25.8 KB (25750 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:988e71b7b9b7c2a7f1f5bbb75c610ff0fae299d25ec548d1619149ab59dcd1c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70654742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26f43a8d3e57af40a322e16fd40d63542fa835f0a084cd427864509f3217dfcf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 13 Jun 2024 20:46:13 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 13 Jun 2024 20:46:13 GMT
CMD ["/bin/sh"]
# Thu, 13 Jun 2024 20:46:13 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOLANG_VERSION=1.22.4
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOPATH=/go
# Thu, 13 Jun 2024 20:46:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 20:46:13 GMT
COPY /target/ / # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112965af61e48c79f6f081b66e8fcc392cd621303fe32a47457e35dbd92041e4`  
		Last Modified: Fri, 21 Jun 2024 05:03:46 GMT  
		Size: 295.5 KB (295459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2259e4bd2629c850a0f37f6d3351f44770f5d4afee65aac3cddcb3bf2a735031`  
		Last Modified: Fri, 14 Jun 2024 19:43:41 GMT  
		Size: 66.3 MB (66270325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93676ef1db8c89860011e8eeae8d68fb8e5d5e669a04a2a907553aab62aff75`  
		Last Modified: Fri, 21 Jun 2024 05:03:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:9c3c87adcc42db7e64e2e4a97996a30f5cf1b7d09debef7cc6df3cf62d0e6b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (25972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b847d7981344838b1e5701a70e927039184ab5aa19aa71e6b7e969940233dce4`

```dockerfile
```

-	Layers:
	-	`sha256:6ade1b3e1f806fa8d512d7e479f2ac3caefe5b0ac299059a099730a470d90541`  
		Last Modified: Fri, 21 Jun 2024 05:03:46 GMT  
		Size: 26.0 KB (25972 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; 386

```console
$ docker pull golang@sha256:33e46b7613e65c58b33b84873bbf23e33616a6a0cacd0b5fd9f06b446a2765b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71107025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff18d154be292a3f0cef04e34345372a16244be5f9b0f7e44abe6d8f98cc1b82`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 13 Jun 2024 20:46:13 GMT
ADD file:cd0e8f9dc9e579bd0c884d2c92e4773391bd73d8302d6f4a9bca0796e7ff9a77 in / 
# Thu, 13 Jun 2024 20:46:13 GMT
CMD ["/bin/sh"]
# Thu, 13 Jun 2024 20:46:13 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOLANG_VERSION=1.22.4
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOPATH=/go
# Thu, 13 Jun 2024 20:46:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 20:46:13 GMT
COPY /target/ / # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:354eb832d25d95145569d0a3a573fb95b8350ee897d5b90a2f67ec1157706ec2`  
		Last Modified: Thu, 20 Jun 2024 17:38:50 GMT  
		Size: 3.5 MB (3469470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77cf9d7129e3b7a6e7ee91c59691980de1cbfc06b9b3e55f2a5dda0a25ac9c6f`  
		Last Modified: Thu, 20 Jun 2024 18:53:24 GMT  
		Size: 292.9 KB (292878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d423f142b846e34cad754942d9961e223ceeaa092ba25d1bfbe95eb1364c405`  
		Last Modified: Fri, 14 Jun 2024 17:54:03 GMT  
		Size: 67.3 MB (67344518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9be4f0f2960b7c312aba0de8fc11e502c1e6ec8fb8afe41563ae8032a5523f`  
		Last Modified: Thu, 20 Jun 2024 18:53:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:5a82ce6b6b612e8564901e184169ceec0dc20d4bf917faceaec0bb361e293145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b647ee2d0e26014ddd4fe948d9e9371c9f1fca7a2568b2e04b0e92792f90d1a`

```dockerfile
```

-	Layers:
	-	`sha256:e4d0e4586a7d00f407de97fd208bcd4e8dddb5f83a3e86fae3ac83ebeb99efdf`  
		Last Modified: Thu, 20 Jun 2024 18:53:24 GMT  
		Size: 25.6 KB (25571 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:fcbeaf889d8d8229be5c51ba0bfe137385a78abfb6b0f9f229706210ee3a237f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70308555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a29aada7a6be788bd72a0a489b6d821bff868da73eaaabdfb666941e45cd8f3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 13 Jun 2024 20:46:13 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 13 Jun 2024 20:46:13 GMT
CMD ["/bin/sh"]
# Thu, 13 Jun 2024 20:46:13 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOLANG_VERSION=1.22.4
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOPATH=/go
# Thu, 13 Jun 2024 20:46:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 20:46:13 GMT
COPY /target/ / # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477fe0e563a78bfc8789f98753a872bab84abaf1026e276ac6665d797175815b`  
		Last Modified: Fri, 21 Jun 2024 01:47:42 GMT  
		Size: 295.9 KB (295884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2210b2be98c546d98d20cd631f014745f73d191238d22c5e439478550b6727b8`  
		Last Modified: Fri, 14 Jun 2024 17:54:36 GMT  
		Size: 66.4 MB (66440814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfed35a1567d183c45c7e8a04b11d626d4dd085224a9a1f3f9e560e2bdf63a8`  
		Last Modified: Fri, 21 Jun 2024 01:47:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:4de5e3afbb442d3e2b1e139f91e4951163d89f41c2fe2d19735a56612d8ce0bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 KB (25689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9991b45b67a17b7e5f34e7fe3bcb9e03841d8c3b7ace8e096c7d0ec7c96bee0d`

```dockerfile
```

-	Layers:
	-	`sha256:061089abef69390fa54a2ed336488df48fc4ee7155d1db2bf06f9d96e8a7cdc6`  
		Last Modified: Fri, 21 Jun 2024 01:47:41 GMT  
		Size: 25.7 KB (25689 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:9404262844440618615c14a078836662b83d7beec6c36a98a09e8971e9bd1027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70555236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5990591af05bea57ad81712748b92d9d711260a156b902b53877a0d44017d8aa`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 17:57:29 GMT
ADD file:adedc612a3543e3a541be8e74c994fc3782e0f4a762ca77a1e29e6abfc81d7d8 in / 
# Wed, 22 May 2024 17:57:29 GMT
CMD ["/bin/sh"]
# Thu, 13 Jun 2024 20:46:13 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOLANG_VERSION=1.22.4
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOPATH=/go
# Thu, 13 Jun 2024 20:46:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 20:46:13 GMT
COPY /target/ / # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f280e85d15153a8f10f3fa47dd9d639e7a8fc6c1c8795d7123a32a0c36f16f55`  
		Last Modified: Wed, 22 May 2024 17:57:48 GMT  
		Size: 3.4 MB (3368560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6846326a7435bb0812f1761b4d68193b8d5cb1f1bdcdf10bad75ac8e83ec7dfd`  
		Last Modified: Fri, 14 Jun 2024 17:57:15 GMT  
		Size: 293.2 KB (293167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720f2671938fbfe8609ea6b3e22d6f25d4497370e3b0109cc065588d36d42db6`  
		Last Modified: Fri, 14 Jun 2024 17:57:25 GMT  
		Size: 66.9 MB (66893351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c29b40752516671457ed4df74ab1914a01f46486d62b3d38f6ed1151cef79f8`  
		Last Modified: Fri, 14 Jun 2024 17:57:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:bb75836330b6aa9a4b0b70dd050520dd6d2ea9b357b9dfcdf3a1f333144fde7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 KB (25690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63f2eca6cb271b7c85ca62c172b33994f9e2a6b71f190fbfd3c3a7d08fdea37`

```dockerfile
```

-	Layers:
	-	`sha256:5e9735a114c07c3340a802dfcf5292bcd384c5118dce610662424806f1dafbda`  
		Last Modified: Fri, 14 Jun 2024 17:57:15 GMT  
		Size: 25.7 KB (25690 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; s390x

```console
$ docker pull golang@sha256:701e88a9136a0fdeb0326815874796e85c92972e67529125d0a38f9cdd995ab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72160635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8613fc2344ba2a853a5e755598b10b241e947a9a7ef9cda9e3f8e56ecd3d9e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 13 Jun 2024 20:46:13 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 13 Jun 2024 20:46:13 GMT
CMD ["/bin/sh"]
# Thu, 13 Jun 2024 20:46:13 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOLANG_VERSION=1.22.4
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOPATH=/go
# Thu, 13 Jun 2024 20:46:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 20:46:13 GMT
COPY /target/ / # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2dbaf32ffd27702fcbbf4fe4d764f59a796cd2d4f7ea86c0e7975245b7941ca`  
		Last Modified: Fri, 21 Jun 2024 04:04:52 GMT  
		Size: 293.4 KB (293400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54ac55846ff64482893d22cd74289e959d60007f939ee44a6905370f9611de2`  
		Last Modified: Fri, 14 Jun 2024 19:31:27 GMT  
		Size: 68.4 MB (68405222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45e302ad79ac2c0f523d67257e514c47ae55272223df23f6d57e8e6b5d1141f`  
		Last Modified: Fri, 21 Jun 2024 04:04:52 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:94cbc87bdfb7d2c039f8bb436fa4ad0756f9bb622d2fa463d0556405466cd841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a720962ed8b2e36e2a85bb79f0c402ded0570232bbcb8448dadd899bb3f516b3`

```dockerfile
```

-	Layers:
	-	`sha256:195e690d6fdbec98d7e37a09265d61a918be566d8f29abe7838941bd99f07c1d`  
		Last Modified: Fri, 21 Jun 2024 04:04:52 GMT  
		Size: 25.6 KB (25624 bytes)  
		MIME: application/vnd.in-toto+json
