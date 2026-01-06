## `golang:tip-alpine3.22`

```console
$ docker pull golang@sha256:058c8fedf71d4411079547db114a823d707948fb917eecf9014f77112b19b214
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

### `golang:tip-alpine3.22` - linux; amd64

```console
$ docker pull golang@sha256:2b48642ebb662610fc9d60038bf6a08c6633407fe49e98b9cbaa3fc462bebbb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99142478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8286ada7ec4a226304311fe94f2efbe0d6635adab907299ce2a144216b39115a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 05 Jan 2026 20:13:54 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 05 Jan 2026 20:13:13 GMT
ENV GOTOOLCHAIN=local
# Mon, 05 Jan 2026 20:13:13 GMT
ENV GOPATH=/go
# Mon, 05 Jan 2026 20:13:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 20:13:13 GMT
COPY /target/ / # buildkit
# Mon, 05 Jan 2026 20:15:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 05 Jan 2026 20:15:52 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e968272a9f45b213fd074d57c1adea11887303e1fecebed7e1babbf2fd80943a`  
		Last Modified: Mon, 05 Jan 2026 20:16:05 GMT  
		Size: 291.2 KB (291163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff8d0c9ecfcf551b6bfe3152ed041603d59cea546df67e4bc43073bc9a2f5e7`  
		Last Modified: Mon, 05 Jan 2026 20:14:07 GMT  
		Size: 95.0 MB (95048707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cc302c937dc65061c2065efcfeae1e7cbb9b7ca9fcffa8e29cf6a5b66c6fc3`  
		Last Modified: Mon, 05 Jan 2026 20:16:06 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:d99500b5ca4cbed78677c030e85e31bf3d880b551ff3f5c594ba56fc88ad82df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ffabc712373aed44e0cd776a4db800a90d90d195f001eb32290b5714c092aa9`

```dockerfile
```

-	Layers:
	-	`sha256:dccabba410ad9e0769b48c25d3ea463c902f2891e3183940c571f6593d23f282`  
		Last Modified: Mon, 05 Jan 2026 21:24:38 GMT  
		Size: 195.0 KB (194982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b9025af80ce73eda4218daf75c70d643ba815023e538799271c09e68c582148`  
		Last Modified: Mon, 05 Jan 2026 21:24:39 GMT  
		Size: 24.5 KB (24465 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v6

```console
$ docker pull golang@sha256:fc34ad622d45a9a0bb72099892c9190ad953680b60f5c51ab48a870c283e6362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95203150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b082948f668a068aea2e94a4d908a42466b611270a30d81df7177be8ffd802`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 05 Jan 2026 20:12:50 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 05 Jan 2026 20:15:27 GMT
ENV GOTOOLCHAIN=local
# Mon, 05 Jan 2026 20:15:27 GMT
ENV GOPATH=/go
# Mon, 05 Jan 2026 20:15:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 20:15:27 GMT
COPY /target/ / # buildkit
# Mon, 05 Jan 2026 20:15:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 05 Jan 2026 20:15:30 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Sun, 07 Dec 2025 22:05:32 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283d3583857ff19f8d561d2e1be13ad0b5e72639cdb378b90b1dc4753c37eb62`  
		Last Modified: Mon, 05 Jan 2026 20:15:47 GMT  
		Size: 292.3 KB (292335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee32a5cb33f89634bd75c31557c25cc9e27ca00d368d41394d0e87b80ed48ac9`  
		Last Modified: Mon, 05 Jan 2026 20:14:02 GMT  
		Size: 91.4 MB (91406577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66425c882d2f2b4d1f661c46447552cc39216bbb9498dfba04a026c6c7b10b79`  
		Last Modified: Mon, 05 Jan 2026 20:15:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:4195795a6200e7eccc0214b891bba8f268b5c41e41202c0af2f55af40448e9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad73c7d7e626a145acaae5cdd258e4c2f212fd369ca42ef299168902fd1dcbaa`

```dockerfile
```

-	Layers:
	-	`sha256:667f09aae05b1cf497067827e2b7265db9e331a4710db5c6fd3a94060e02c05b`  
		Last Modified: Mon, 05 Jan 2026 21:24:45 GMT  
		Size: 24.4 KB (24362 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v7

```console
$ docker pull golang@sha256:5460ef58d6442ad02a7b5decb25e22152960cffc0dbe9a5be64d0e940874d925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94639216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb7ef48e6b7c533becb8b9799d207e329b8121c48528005af2daa049d0f6665`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 05 Jan 2026 20:14:12 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 05 Jan 2026 20:16:45 GMT
ENV GOTOOLCHAIN=local
# Mon, 05 Jan 2026 20:16:45 GMT
ENV GOPATH=/go
# Mon, 05 Jan 2026 20:16:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 20:16:45 GMT
COPY /target/ / # buildkit
# Mon, 05 Jan 2026 20:16:47 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 05 Jan 2026 20:16:47 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Sun, 07 Dec 2025 13:57:17 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4dfdedd42e5ea6740fbe5011bda229ae574175d7892b93873f05d79b082952`  
		Last Modified: Mon, 05 Jan 2026 20:17:08 GMT  
		Size: 291.2 KB (291210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e6b96a7f28bc62643bd07c2486d1581cdd92ecf9bab96beac98ff164054e9b`  
		Last Modified: Tue, 06 Jan 2026 02:36:10 GMT  
		Size: 91.1 MB (91126293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e09000b39f5a5711c8cdfaf80323079b030512adabf0cdbb0b0a2fa48d994c5`  
		Last Modified: Mon, 05 Jan 2026 20:17:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:adc779bdba8d3f78e603392264f80c0b724cf815aed17f8f428481e9d1991bca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 KB (219563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5652c23099146c6e4339438dab22f948d126a8e2ef8373c0ac0ad6d8d130467b`

```dockerfile
```

-	Layers:
	-	`sha256:63ea667b9d331b0f43a58f0fba5f394ab1706682a383c1ace7c5015c9225fd1a`  
		Last Modified: Mon, 05 Jan 2026 21:24:53 GMT  
		Size: 195.0 KB (194986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fea90a7cad00d34befc80277d430428daba0ba0d1676c40721bca43d4686ecb`  
		Last Modified: Mon, 05 Jan 2026 21:24:54 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:0429a73a2f55752d8565f2f67639b9627aa7bff69c63857a712fbc2596c7ae20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94566813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15dc343ddcacd317dfd3681b96fcd09bef34bde29f7a32e92caeddd74ac9b729`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 05 Jan 2026 20:13:17 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 05 Jan 2026 20:12:38 GMT
ENV GOTOOLCHAIN=local
# Mon, 05 Jan 2026 20:12:38 GMT
ENV GOPATH=/go
# Mon, 05 Jan 2026 20:12:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 20:12:38 GMT
COPY /target/ / # buildkit
# Mon, 05 Jan 2026 20:14:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 05 Jan 2026 20:14:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4274c2dcefdb0b7831f2bf7d51c6eefea8f36b801510ab6e315a937f826ecdd4`  
		Last Modified: Mon, 05 Jan 2026 20:15:07 GMT  
		Size: 294.1 KB (294118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ea799c03d09b63583e3ebd313f2aacd577c4821e87f618e936a7b9c3c7ca14`  
		Last Modified: Mon, 05 Jan 2026 20:13:38 GMT  
		Size: 90.1 MB (90134470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ebb5aa8af5c0c9eb8edfb0900cdba065fb55664f74ff398c91c0599861a64e`  
		Last Modified: Mon, 05 Jan 2026 20:15:07 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:defce7a14b448af3bc904736b02e420591c3d1c16a0d737d3ebc0f18c1bf0d49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 KB (219615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05e4642ca8399814bcfa9f0ec6906e7ba9d7324c47b41aa81a0c4f8174d09105`

```dockerfile
```

-	Layers:
	-	`sha256:9c1372d6876b54acd046fa548ded0912c10a10179ce0137309643022aca14d5b`  
		Last Modified: Mon, 05 Jan 2026 21:24:58 GMT  
		Size: 195.0 KB (195014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb551dc4d8458444e713c660dc0b5ea7332d8b35a8b42de885938b05a03eafa6`  
		Last Modified: Mon, 05 Jan 2026 21:24:59 GMT  
		Size: 24.6 KB (24601 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:45f9dae16b2afc768cdaa2922a536f1d0d2f67106d7f24c1bf11b1f2707f7d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96855534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a96ea77b7fc7b8885961f42c7759cb213f34914bf354db763533558c8a30aad`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 05 Jan 2026 20:15:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 05 Jan 2026 20:14:42 GMT
ENV GOTOOLCHAIN=local
# Mon, 05 Jan 2026 20:14:42 GMT
ENV GOPATH=/go
# Mon, 05 Jan 2026 20:14:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 20:14:42 GMT
COPY /target/ / # buildkit
# Mon, 05 Jan 2026 20:17:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 05 Jan 2026 20:17:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Sun, 07 Dec 2025 14:06:47 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0affb9f3c5dceb21aa63c8478b68728637801566a4b22662740c7d098369e0e1`  
		Last Modified: Mon, 05 Jan 2026 20:17:32 GMT  
		Size: 291.6 KB (291635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7adeeca0c05b570f562d36e2ca80fe92bff9d338efdfb31d2c7a616347bb0c`  
		Last Modified: Mon, 05 Jan 2026 20:15:35 GMT  
		Size: 92.9 MB (92944811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0889cceb902c7659a907f6eb81efc23024dbd967aa8aab2c462b1316081653`  
		Last Modified: Mon, 05 Jan 2026 20:17:32 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:2acbbce6e78ea2a044090416d95b6679dd1efe61b33ce0046ad09594dc3f8fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83dbbf50598121f3f41ba10d10d0e6aba103e450bf2c49bfd02a14b453d682f2`

```dockerfile
```

-	Layers:
	-	`sha256:3dc8472708dd072b12f2411fe0bc688dd149a294fce12e8dddf39d192b8f1f05`  
		Last Modified: Mon, 05 Jan 2026 21:25:03 GMT  
		Size: 195.0 KB (194951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f07fb7716b2c8b8fd1ffcd48050287c195a8c059eb6b0584e20f1543b46bbc0f`  
		Last Modified: Mon, 05 Jan 2026 21:25:04 GMT  
		Size: 24.4 KB (24432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; ppc64le

```console
$ docker pull golang@sha256:5e14ee38bae3a337dc5786ca1d554f4c6f335328b1cbdf32dbf52ca1f3b53715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.7 MB (95707633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c1a30ee328757418895c0edfdb993ad6e8f610d4edacd7bcf2ff3f3a32ee08`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 24 Nov 2025 22:43:33 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 05 Jan 2026 20:13:42 GMT
ENV GOTOOLCHAIN=local
# Mon, 05 Jan 2026 20:13:42 GMT
ENV GOPATH=/go
# Mon, 05 Jan 2026 20:13:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 20:13:42 GMT
COPY /target/ / # buildkit
# Mon, 05 Jan 2026 20:19:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 05 Jan 2026 20:19:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Sun, 07 Dec 2025 14:06:45 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64958bce21ae47528776dd8bd6794140e1f5086c72ae8807ba8f48bb37fce769`  
		Last Modified: Mon, 24 Nov 2025 22:43:59 GMT  
		Size: 294.6 KB (294592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd0091ff10375737167c3b5f9f5d9decb460a2e2aef6a9ae134067abb7cbf2b`  
		Last Modified: Mon, 05 Jan 2026 20:15:39 GMT  
		Size: 91.7 MB (91680642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84fb74ace9a8976166d6d75144101663fcc3af67968f24ee4320a7b7c9eb792a`  
		Last Modified: Mon, 05 Jan 2026 20:19:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:9706bb0ff574ddc7b45fcf47c3fc074416d5a45aa14ed487bf6b5bbbb34ffca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 KB (217407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d35f1a2450d78e53d342108919353873867ca9d0150c797f6cd7d2819b1c549f`

```dockerfile
```

-	Layers:
	-	`sha256:eddefab2f1e81036d4b8acfec4d8bbddb3f0886f69a00c84ec8ccc070493cb4e`  
		Last Modified: Mon, 05 Jan 2026 21:25:08 GMT  
		Size: 193.1 KB (193069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d337964a64f7710ec9476167a0034865b211d0a796b67d90eea3cf328ea94ed`  
		Last Modified: Mon, 05 Jan 2026 21:25:09 GMT  
		Size: 24.3 KB (24338 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:2dea4f8a596f73821b105cb7594fa8464f7e9e9db222238867a2263b369d39a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96119803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbfc575f5bd066367f5b7aa9571b3de67531da4de486a32b6b34d057172700cd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 25 Nov 2025 07:20:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Jan 2026 01:07:38 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Jan 2026 01:07:38 GMT
ENV GOPATH=/go
# Tue, 06 Jan 2026 01:07:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Jan 2026 01:07:38 GMT
COPY /target/ / # buildkit
# Tue, 06 Jan 2026 02:30:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Jan 2026 02:30:32 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Sun, 07 Dec 2025 22:49:04 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a984176d166c6f9d398140e2c603deed3f1a52311d2a418b830c1cfdaffb3c`  
		Last Modified: Tue, 25 Nov 2025 07:22:38 GMT  
		Size: 291.5 KB (291523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c89a20e33326bd3dc067a98c23f95a9f71a46db050c57b5d95bf4165852889`  
		Last Modified: Tue, 06 Jan 2026 01:15:07 GMT  
		Size: 92.3 MB (92312883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77550d05104d9262d6266ba959a9969d5ca4a9676385393a189890d234d1963`  
		Last Modified: Tue, 06 Jan 2026 02:31:53 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:efc605234f9181ad44e0876ac88da9d431546bd74999c1c86c36e76188c4a292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 KB (217576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e7abe999fbd0a7c9e463265d451676a18e9b3f8f1b3c2d8d6dc375ea0e3f9e`

```dockerfile
```

-	Layers:
	-	`sha256:ee321cd36964ee83537ee45421b6ec880bc53875cd8dc1655129cee023de59e0`  
		Last Modified: Tue, 06 Jan 2026 03:24:03 GMT  
		Size: 193.1 KB (193065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37a4e8f9d6d7d09a26fe59ed1c504f77215223b94cb4cdf8bf831105c3f64d9c`  
		Last Modified: Tue, 06 Jan 2026 03:24:03 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; s390x

```console
$ docker pull golang@sha256:4f2b490b4bfe202f7140fdafe4224f6ee3166ee8052d293d4821f09cd37c6860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.2 MB (98166051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff6075a293912b442753be549ce9033ffb955f2794b82c28a10115da384a71b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 05 Jan 2026 20:14:04 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 05 Jan 2026 20:13:53 GMT
ENV GOTOOLCHAIN=local
# Mon, 05 Jan 2026 20:13:53 GMT
ENV GOPATH=/go
# Mon, 05 Jan 2026 20:13:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Jan 2026 20:13:53 GMT
COPY /target/ / # buildkit
# Mon, 05 Jan 2026 20:14:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 05 Jan 2026 20:14:06 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Sun, 07 Dec 2025 14:06:46 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b23ac86cc82c0a9dd30d2f1655cce6ca1680bd3145eca5186858d900cd9711`  
		Last Modified: Mon, 05 Jan 2026 20:14:40 GMT  
		Size: 292.2 KB (292155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c1a057ff0ba348d0b96ad5fd481980beed6ee225e3440d5e3c814a12014a9d`  
		Last Modified: Mon, 05 Jan 2026 20:14:55 GMT  
		Size: 94.2 MB (94224494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b9090a67ee14781b8b29a381458d8bd4dadcb434ae8d5d82c5751a066457ed`  
		Last Modified: Mon, 05 Jan 2026 20:14:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:2aec862dea7d41ce6f001c05d878b38a38c994775cd5f760f0248b99e417fb2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 KB (217323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76784c92a13ed096c9f8975abe637cdf01be2bf6bb9ba993d5c5262de8ccd131`

```dockerfile
```

-	Layers:
	-	`sha256:28adc4e8914facb49fb0833faa8b7a499d2a8928e10b7d8545177ee1bceb4e3c`  
		Last Modified: Mon, 05 Jan 2026 21:25:13 GMT  
		Size: 193.0 KB (193031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99425b9dc7fd44ff91e2b0272e10a35558745c893d5f3001489ef88e894f58e9`  
		Last Modified: Mon, 05 Jan 2026 21:25:13 GMT  
		Size: 24.3 KB (24292 bytes)  
		MIME: application/vnd.in-toto+json
