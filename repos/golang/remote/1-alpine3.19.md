## `golang:1-alpine3.19`

```console
$ docker pull golang@sha256:36cc30986d1f9bc46670526fe6553b078097e562e196344dea6a075e434f8341
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
$ docker pull golang@sha256:e6f02c8e85db39f020c4325dbe9919ac3a73fa1df0f15540c33bd446e33290e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77751741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffe7976590a8f93acdff95b32fa458f4424da5b67e1ff513ca01f9d29ddf4090`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:13 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Fri, 06 Sep 2024 22:20:13 GMT
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
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d629177f280090b0f20da0b2ead322608920dd3bcb2f11b89ccad3c8b150ab`  
		Last Modified: Thu, 07 Nov 2024 02:59:14 GMT  
		Size: 292.9 KB (292878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79bddf330f7de2b96b69740174bc7152350ef81439db2dfa776fc3a9365dc80`  
		Last Modified: Thu, 07 Nov 2024 02:59:16 GMT  
		Size: 74.0 MB (74038999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cacea6bcfb84c769234d38ff9b139d4c105aa35f3f11e4442cd111faab6d9f7c`  
		Last Modified: Thu, 07 Nov 2024 02:59:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:19082efc07a70504f7b15bf2c1a6070e65f4668a24ced98f8e148fa193fdbcd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.7 KB (237700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fead99854e140f031ba055be71da8e8bc808499e2a66af9e16bdfa3db1b21b6b`

```dockerfile
```

-	Layers:
	-	`sha256:b88c2b2f041212058ccb007076fe2bcbd98ff97dd1e76d0ee952db16cb49c4cd`  
		Last Modified: Thu, 07 Nov 2024 02:59:13 GMT  
		Size: 213.0 KB (213043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0a8508090f2f3629617d6aae9e1d16005b3d1aa2487a80be231f217877f7081`  
		Last Modified: Thu, 07 Nov 2024 02:59:13 GMT  
		Size: 24.7 KB (24657 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.19` - linux; arm variant v6

```console
$ docker pull golang@sha256:1a05bac286a348e7a8dda1ee9594dceb09897bf7d1ed1c0a48d8e5fd90bc3ed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75654770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804b7957599587647164b0a0caf3776fb707ebe5f243781ff275332d24227f0d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:26 GMT
ADD file:87d4cb9e99b4a12939a030198a62d49f1c5b7856f27d62fea0e948cd2120d51d in / 
# Fri, 06 Sep 2024 22:49:27 GMT
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
	-	`sha256:8922ced57063579c37aeb21c1c664433762d26f8051e187a63b559c21b36da53`  
		Last Modified: Fri, 06 Sep 2024 22:49:59 GMT  
		Size: 3.2 MB (3176391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163a189aaa8881b35f02064df0565f1c166dd7085fb308b5414059d2a5ec1777`  
		Last Modified: Sat, 07 Sep 2024 02:31:12 GMT  
		Size: 294.3 KB (294282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6930abd3e962e7fc186f25f91e441a0655bacbb61cdd3456fbbb1368d3ebbb4`  
		Last Modified: Thu, 07 Nov 2024 02:59:03 GMT  
		Size: 72.2 MB (72183939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d2a65e06c1efc67a8d72941dcb8ff1cc51ac48620b20db40d97cca66a0e44d`  
		Last Modified: Thu, 07 Nov 2024 02:59:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:0b20b7a7c3b112a11c2782809e44086c9a2d6a2301b6ded7d52dd029c431bc2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 KB (24538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45f7e859d5cfd17de3166fd5b68e60c671cecef7730138611da9bb51bdc2697`

```dockerfile
```

-	Layers:
	-	`sha256:811eeb9146e5c72e1666df2994c5e6b4302c7a127eba2dd113eaf642d455296c`  
		Last Modified: Thu, 07 Nov 2024 02:59:39 GMT  
		Size: 24.5 KB (24538 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.19` - linux; arm variant v7

```console
$ docker pull golang@sha256:4b01bfa7e7251065c057f6195400b9494c8c7fa0ea2f3acda9fa9043d9a8f649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75405031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08dfe10b032193351fbbbc1cc5a572526442b60210141603cd960aeb56fdcc9e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:05 GMT
ADD file:a0a04eec8c7b34f27431bfd6edc27b4c05f2174daf93e40c263717d2469dcebd in / 
# Fri, 06 Sep 2024 22:08:06 GMT
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
	-	`sha256:426a5537ab470cede64a1b269dbc9f485fa674bec59555cdaa5a1c96e6675b0d`  
		Last Modified: Fri, 06 Sep 2024 22:08:37 GMT  
		Size: 2.9 MB (2927664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d3d0ab8c3799b4586924b10a2a29606e4c0f7404f21d3271d9b7cea2db554a`  
		Last Modified: Thu, 07 Nov 2024 03:02:24 GMT  
		Size: 293.1 KB (293123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e990400f8c0342109351b2ea2dff891387190e755f29d02b0f474578fc3d222`  
		Last Modified: Thu, 07 Nov 2024 02:59:45 GMT  
		Size: 72.2 MB (72184086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139722807d64971fb17fbf7512ef471872b957785f127936771b73acd9176393`  
		Last Modified: Thu, 07 Nov 2024 03:02:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:d5b6ac9bf78f865e87904f8885209caec8843d7e536bf411650b9af9c0284a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.8 KB (237796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24ebf5eeb28ce7143a45745ea01d2f4a434f8cd380dc6f48aab6dc2768d2e8f`

```dockerfile
```

-	Layers:
	-	`sha256:42d7d0815e14e4e708a6ed760f45c6086a4c2d9ac17cae8512b1f118e82ddc46`  
		Last Modified: Thu, 07 Nov 2024 03:02:24 GMT  
		Size: 213.0 KB (213043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b426640101adc1ce188fd3831f8598758d4c7c37af5bb173fc8fc00bf4f07fd2`  
		Last Modified: Thu, 07 Nov 2024 03:02:24 GMT  
		Size: 24.8 KB (24753 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:571375ba0a63b1ae292a8ff4870f84081da6a3745f9951e99c0f37cea9937d99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74324245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9da85817852f9bea611eb4ef140123327326c78ba9a8835569c4fdc22b967e3c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:16 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Fri, 06 Sep 2024 22:44:16 GMT
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
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9f3edd7ef5a80d8856bad2c6d36f4267e95460182008979a4f0f4a567832a7`  
		Last Modified: Thu, 07 Nov 2024 03:01:24 GMT  
		Size: 296.0 KB (296036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323003b0d8ad8001283c9881b96c87e9fa38fb378aa4de93c4defd3899f30d2a`  
		Last Modified: Thu, 07 Nov 2024 02:59:17 GMT  
		Size: 70.7 MB (70668948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d15d29ef5182ec2c2ab3958aa4103205be5ff15cff8be8a12793fec2fff1b0a`  
		Last Modified: Thu, 07 Nov 2024 03:01:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:458271f4a904a06b4249557c5c76d804c862ac6931185d8f012453e520a403e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.9 KB (237884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9434c749274fee5afb005c627c63b2c8e5f480e5b754eaabbf5b6807b5ef88a7`

```dockerfile
```

-	Layers:
	-	`sha256:ca9e5862d52dcf952989ecbe057f2e4bb5e49dc7f64c9f14bd573a5acd4f3317`  
		Last Modified: Thu, 07 Nov 2024 03:01:24 GMT  
		Size: 213.1 KB (213099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27f8463c3ecdb6fd7ec25e125bf7f3313c74caa546de1d220e39bfc271c2c079`  
		Last Modified: Thu, 07 Nov 2024 03:01:24 GMT  
		Size: 24.8 KB (24785 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.19` - linux; 386

```console
$ docker pull golang@sha256:d1617fa64edaac255d56c00651246f5538fc0bc2d89ce4dcb9cdc2d5b09da5a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75455300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee177cd7becbb301abd6005c33bc72f55f6023ed0bfb771466e78b0b9dc1186a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:25 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Fri, 06 Sep 2024 22:41:25 GMT
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
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d61042a962db37857687a3087fd61d24c7c01d2f1e6339351010bda93247043`  
		Last Modified: Thu, 07 Nov 2024 02:59:08 GMT  
		Size: 293.5 KB (293520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d309da02a5efef0a1926ae8de3247932524a303115a90abb23504c4cffb291`  
		Last Modified: Thu, 07 Nov 2024 02:59:09 GMT  
		Size: 71.9 MB (71908016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c727e6346fbd961a29dba6afd42b5fa8482a9237adba298df500ea2fe236585`  
		Last Modified: Thu, 07 Nov 2024 02:59:07 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:c5c937073ea9d8ed2bb10778280b7ec050a7345e69cee1c8f522b469d8481ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.6 KB (237605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b438697982febdeaaacba47250153656abd0a9627503d0d51583cfcb47c9e64f`

```dockerfile
```

-	Layers:
	-	`sha256:04512e2029238010606c9f3b9a43aac71251ada1bfd77ee0bc5216d2ba20f18b`  
		Last Modified: Thu, 07 Nov 2024 02:59:08 GMT  
		Size: 213.0 KB (212982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28ebc97db66129f12343fcb18ffa98d22aeabfdc086e5c14899aa7c7c4afc21f`  
		Last Modified: Thu, 07 Nov 2024 02:59:07 GMT  
		Size: 24.6 KB (24623 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.19` - linux; ppc64le

```console
$ docker pull golang@sha256:63bcfd948967356b49b4db63808b4cf982527bf92ac355efa5b814b706358a72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74489548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997132073417880f26cc1a881c4a634556bd1abaf6c5e97dd97a99ca4277b50f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:13 GMT
ADD file:2b460e2f1af1fd81bcf839fbca42c282e18754a310086d2d55772cfcaff3154e in / 
# Fri, 06 Sep 2024 22:26:13 GMT
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
	-	`sha256:1274ef399099f48829c82f23090a3c36444839648f7cf9fbf44c7518257fcdd2`  
		Last Modified: Fri, 06 Sep 2024 22:26:51 GMT  
		Size: 3.4 MB (3364467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5dc63221573a8b294ca8c6ce62fbf44a0b92bd6a1d682f50231e8159d46f4cf`  
		Last Modified: Thu, 07 Nov 2024 03:02:26 GMT  
		Size: 296.4 KB (296446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d45dcd888e3183671630e662953341e3111584ee0e6ca4f0d40e50580ea2de`  
		Last Modified: Thu, 07 Nov 2024 03:00:09 GMT  
		Size: 70.8 MB (70828478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd557691bd427623af5c31efafa6dd41bc4a22a4753999d61a851edfffd3d4eb`  
		Last Modified: Thu, 07 Nov 2024 03:02:26 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:b042af04b4310f9a365e59f9d7e2e98876b730ca9169925eff302c94a71f0f96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 KB (235858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0c0fb3dc591354ee9759ef29b211106cd7694bd086490ae0caf67c3c406d605`

```dockerfile
```

-	Layers:
	-	`sha256:73fa27038bc0dd60b12774e3aa3ec39d178639c2983493494f1cf128dc525525`  
		Last Modified: Thu, 07 Nov 2024 03:02:26 GMT  
		Size: 211.2 KB (211159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db4d9303b4fa9df989ac54b1a176e364c4d74b521d605e7ee60c73eedb543783`  
		Last Modified: Thu, 07 Nov 2024 03:02:26 GMT  
		Size: 24.7 KB (24699 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.19` - linux; s390x

```console
$ docker pull golang@sha256:5960b2f9a4dca99df9c68cf0e2ec0b0d005506ff58d8530be8a0ad9081e7c6f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76497483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cd5df3b3096a35907c0ac302ea91b8d1a2360de52f9b7374e8a804dc2f0fec3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:26 GMT
ADD file:accee20143ffbe803d23675898d25fedbb25c04fcc9f4ddaa1ba5f066c5ae260 in / 
# Fri, 06 Sep 2024 22:48:26 GMT
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
	-	`sha256:dbf93dbda29c680e293e8229956c663ae9d4e8435d70335c363568788915cac5`  
		Last Modified: Fri, 06 Sep 2024 22:49:04 GMT  
		Size: 3.3 MB (3253357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b516e307f15b4dca6bd73d26121556714328ff8d682372187157e8c6bbb1707`  
		Last Modified: Thu, 07 Nov 2024 03:05:55 GMT  
		Size: 294.1 KB (294076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8899e076c675a549e2d1bc5d05ac9fc56f919b55bb9ec6d441d414eb5acb3e0b`  
		Last Modified: Thu, 07 Nov 2024 03:03:52 GMT  
		Size: 72.9 MB (72949892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f13968438d76e6ad20965e49579f62824a974a29277d2342e01cabfc2da48e1`  
		Last Modified: Thu, 07 Nov 2024 03:05:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:0acd887bba1aef4bd3c11886d6afa381a1aa623e679b08f968fe36d30db129d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 KB (235746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be9522e9a1e91a9b0811dc58c1f74a6a3af1d945b28d03bbbe90671bd05553b`

```dockerfile
```

-	Layers:
	-	`sha256:8cb72a6eebcd3e92bbe54b8583f7257e88fcec19b4cbec966d3d0a653cc9c223`  
		Last Modified: Thu, 07 Nov 2024 03:05:54 GMT  
		Size: 211.1 KB (211089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a1fa4caa8c83154dced00f3a3f0003dbfc07ee084bf120c006450e3abe44198`  
		Last Modified: Thu, 07 Nov 2024 03:05:54 GMT  
		Size: 24.7 KB (24657 bytes)  
		MIME: application/vnd.in-toto+json
