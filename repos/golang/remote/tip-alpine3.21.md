## `golang:tip-alpine3.21`

```console
$ docker pull golang@sha256:6976073fbe392e73983da6967a9ec9826a1c6e04d0215baa09283ed0c94686e4
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

### `golang:tip-alpine3.21` - linux; amd64

```console
$ docker pull golang@sha256:7ad5401746f2aa69d1a46a8b11bfb976f5686ba9a462ebc8d1eb0d3f6472a579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88528916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a2c2c5e9cc2b2d2436141dc9444be4d3f858c5443454a58e4cd2513cf9312f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 06 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7d596846178f48ecf89e51a378b7abc94f10a412ee1db4d440994445c2f6c6`  
		Last Modified: Mon, 06 Oct 2025 21:03:30 GMT  
		Size: 291.2 KB (291172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df330a3159ef2a0bf41805e9465d878d806cf4287e8fdd250ddbc3e024a94e45`  
		Last Modified: Mon, 06 Oct 2025 21:03:35 GMT  
		Size: 84.6 MB (84600016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643a267e6fdbb6a1b8329064aa993e0d53641b1f561be069ef5b25405b465a69`  
		Last Modified: Mon, 06 Oct 2025 21:03:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:99fb65d29ef7cc19a1bbdb7f7274f6ef8905ecd7ae7b2157de0e93081e57507b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 KB (218324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05279bcc695646de99491a49ce2384ad9b199d6532880c5df83422ac4fd5a38`

```dockerfile
```

-	Layers:
	-	`sha256:7edd72bc1fb3eedc25d27d3d2593a3ad3ea4108b4bf9e8321285d40aeaa59694`  
		Last Modified: Mon, 06 Oct 2025 23:24:14 GMT  
		Size: 193.8 KB (193816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf9bebfee43359855d73c21d99a0913ad0c6e96a25ced2185e2a98bc2417b973`  
		Last Modified: Mon, 06 Oct 2025 23:24:14 GMT  
		Size: 24.5 KB (24508 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v6

```console
$ docker pull golang@sha256:ad74b99fbda2e87046837dd5b6b0d41705f05722b8291205ff075c2bf61b0390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 MB (85457463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d97a6f64106f892abf509ebce2ebb2bab4bb6217b52760251b64574b5064c61`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 06 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ca0c331561564c536ffa9246944bb50ac21d3fb11fe66c38baad97fdd1f05719`  
		Last Modified: Tue, 15 Jul 2025 18:59:41 GMT  
		Size: 3.4 MB (3363814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77dbb399e49872ab4217b918166a3c380427bdfccde08de3c30de42c8c4ab10`  
		Last Modified: Tue, 07 Oct 2025 20:12:07 GMT  
		Size: 292.3 KB (292330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4ca929e1e82e3da2a8d3fe64f9852116fdde16db4405daccb287d008513ea4`  
		Last Modified: Mon, 06 Oct 2025 21:06:14 GMT  
		Size: 81.8 MB (81801162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe3110621a5707d289eaf9d6a06c00d600488e28c36fbe1e852484e4022d058`  
		Last Modified: Tue, 07 Oct 2025 20:12:07 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:0ca7d2b25c04ad4fc6978f664712fa3d6f068ae0a167409ffb5dbb1fd73d4b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e7931bb8d52d357dcf5533b1ef1a9e5197c5027392cabcfc838d5c096a6108`

```dockerfile
```

-	Layers:
	-	`sha256:7d525bde6a5b3faff40a604671c2d545e25096f443ea169e6cf4871b71245ed2`  
		Last Modified: Tue, 07 Oct 2025 20:28:51 GMT  
		Size: 24.4 KB (24405 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v7

```console
$ docker pull golang@sha256:81d1b5f5ef13d5559b3a7f5869ccdea2ea57b5b623b12a3ae6f7543083b3972e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.9 MB (84938135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a4b6df60cc0b513b0c2d55647c972dacfd903c14ccd277a1ac4e23e4786c73`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 06 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a96f521d793eec1dcb2b825985eb01c309edb500ebd753a2f84cb9430f05802f`  
		Last Modified: Tue, 15 Jul 2025 18:59:46 GMT  
		Size: 3.1 MB (3096871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93b3dca56fd32dbbb2ab9f4c55c793b57b77b34d4dc4e046053e7251e1b87b5`  
		Last Modified: Tue, 07 Oct 2025 20:15:08 GMT  
		Size: 291.2 KB (291214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113454a922f3bf5f9a74062c96cd1b1dd4f7636e5e5993fd895b9a087d38b9c4`  
		Last Modified: Mon, 06 Oct 2025 21:04:32 GMT  
		Size: 81.5 MB (81549892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94723e0976e372cc5b03c0aa94c6c3da666ac7ab93851f1764ef9d99b5eb0887`  
		Last Modified: Tue, 07 Oct 2025 20:15:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:8af1b7e721e1e79a3eca568d278f315cb9a296c048fd83a9612eb6554fe7cb4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.4 KB (218442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:605d0ba0a501b42382bfa8c0300697873c48fa7791ff75cd2821438edefff6e0`

```dockerfile
```

-	Layers:
	-	`sha256:6cf889556074dc0b884e1fd8f6de2af978337b35203813d2eeee91b6e4d985b6`  
		Last Modified: Tue, 07 Oct 2025 20:28:56 GMT  
		Size: 193.8 KB (193822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1621d9f2e34519153f733de4f1e67a04044c5ebdb5f51b316d49a6196d74f502`  
		Last Modified: Tue, 07 Oct 2025 20:28:57 GMT  
		Size: 24.6 KB (24620 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:fe0cbf8b9767ddb39e98c2938e2971cff71be7c786535af5f5cbf8cfaa77c493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.8 MB (84813052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d868fdad94c71447e6b20b1b8872084efd13382cd158faf8e39c633a60135f4e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 06 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545060b84a85a802247ebb52434f642d0b9cdd7a08a57f1ddfdb245e5ffc1995`  
		Last Modified: Tue, 07 Oct 2025 20:13:09 GMT  
		Size: 294.1 KB (294107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ae6f3de502e34feaea64f03c33850b0abe91d2931d0f357546a0b84a633dd1`  
		Last Modified: Mon, 06 Oct 2025 21:03:39 GMT  
		Size: 80.5 MB (80531850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab81e14c138077446344fcf1ffe7e74cdbdfd64f082694cedaac20e77c09115`  
		Last Modified: Tue, 07 Oct 2025 20:13:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:143151cd903bcf147be87bca7bbed603459eede4a9366ab6153fd01ff17f5841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.5 KB (218492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3318262f8a07a8de5c444524ba01b6e03e2a5a7d17d40a8479f9dd8104c7004f`

```dockerfile
```

-	Layers:
	-	`sha256:eeb4ed02c5fff2f7fd01fb132a0b1668ca329e52ce8d746c4dded67fa0f529d1`  
		Last Modified: Tue, 07 Oct 2025 20:29:00 GMT  
		Size: 193.8 KB (193848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d70f809907bad8056716169b0d125d87fa6bf306e9418d5f9f74e553ea866b4`  
		Last Modified: Tue, 07 Oct 2025 20:29:02 GMT  
		Size: 24.6 KB (24644 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; 386

```console
$ docker pull golang@sha256:17a622aab45f7c12583b89ce0478d272c704dce59b7bc49cb89a6b2867b9d39a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86897982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a348aafe14661a550d9f4a243483a708e2a948d42a6560da8d9db933b621010f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 06 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:47ad0adcb4aa253584437783c542bfbd2276c07a7a0b7487bb26f9b2e80cba73`  
		Last Modified: Tue, 15 Jul 2025 19:04:30 GMT  
		Size: 3.5 MB (3460726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fdd7beca99edc17dbb5f50624078d1b1160d955d5da626fdbc2865d2ad9c376`  
		Last Modified: Tue, 07 Oct 2025 20:16:06 GMT  
		Size: 291.6 KB (291632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1c0a8fc757d99c51188cdf4bad50d211862dd20e9507d39b31fbbec343ddd8`  
		Last Modified: Mon, 06 Oct 2025 21:03:40 GMT  
		Size: 83.1 MB (83145466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b771364e6bfa2691e0e3f2d4c0bbee3e10a9685ddedb51693df42dcd322594`  
		Last Modified: Tue, 07 Oct 2025 20:16:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:64a0722b1b14a227d9f2034899b3bdcd97dc049d07f8f5c9226f371b097eca6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 KB (218262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350660c29bde38b1cd809df84401be323df98136ac8b0345ccf2cb109f73271c`

```dockerfile
```

-	Layers:
	-	`sha256:04149a26280d01c16b1230e1c3f1b53b596221658b513a1106c9f8b70ac3598a`  
		Last Modified: Tue, 07 Oct 2025 20:29:07 GMT  
		Size: 193.8 KB (193787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11269a6be6f000b95e11b98639452229337ebbe9e85f67cbd50525223401bfd2`  
		Last Modified: Tue, 07 Oct 2025 20:29:08 GMT  
		Size: 24.5 KB (24475 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; ppc64le

```console
$ docker pull golang@sha256:b691766106c9fe58b53b991826aacbe88f4850c22fbaf669240c31e16bbc609e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85731294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ccf76a1c94f1043955db305c31e65e93d96e008f001ad9626b91ca8711ab3c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 06 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bf93837577694839723892fa29fd11013552ac59944071e2341ac6d6d9876d29`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.6 MB (3569125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c72ed30b4440614b477e3a87c9a33476b9d0b437a968436db8903fed6fcee5`  
		Last Modified: Mon, 06 Oct 2025 21:18:20 GMT  
		Size: 294.6 KB (294580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734f43290ecdfba214453228a07057302573d0be977b7f6d3aeae38f2799df4e`  
		Last Modified: Mon, 06 Oct 2025 21:05:37 GMT  
		Size: 81.9 MB (81867431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4979bd9db1a7c6a86675796b8a6cafd6088aa86fb06a3e43e30cd9866e8848`  
		Last Modified: Mon, 06 Oct 2025 21:18:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:dad9817aa51dbaaf96c223e5b18d41d18040fbbca8d7220ad251197d733a35b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 KB (216454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bab4e4d8d4fb721ef7860b10a5d13dc771ea4b0370637f0d9dcc2197281c7da`

```dockerfile
```

-	Layers:
	-	`sha256:383f0b77437b323b5aa64711633650453733f251e261edbec79b2f78aa825363`  
		Last Modified: Mon, 06 Oct 2025 23:24:32 GMT  
		Size: 191.9 KB (191901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d164206de9214e382beba5c4909faea3b172a815e6db73f15e3b53f25ef2e744`  
		Last Modified: Mon, 06 Oct 2025 23:24:33 GMT  
		Size: 24.6 KB (24553 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; riscv64

```console
$ docker pull golang@sha256:dc8bf9f3076cfbe7e9a01b239d10b5a56a88a32f51db1953dcf3578d8ab575f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.9 MB (85874653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89baaab6b5d95c890e2fea78bf56944811bb4174b354d3ca72aa28593fd90530`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 06 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66587a4ead2af4b3777a88f71fff7f8fb2d28fecc6835536cfbd5f10d19b67b0`  
		Last Modified: Tue, 07 Oct 2025 14:56:06 GMT  
		Size: 291.5 KB (291518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58fd0ce2ab28438bdf94f05f192ab71a6b801a6c5d6e3d4dc6d664c820e75f2c`  
		Last Modified: Tue, 07 Oct 2025 14:09:36 GMT  
		Size: 82.2 MB (82233887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0e9dc401db6b547151558896af20f8b9ccdb3710d93a2e2ad72eb60b1f06d2`  
		Last Modified: Tue, 07 Oct 2025 14:56:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:680bedd0857baa651437a254bcb8fde952878016a739ace6ca9c6cbca4a857a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 KB (216451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6427cc558d81b544d39bd65188b5f50edbe2d727f35156be34314743fdfb4c41`

```dockerfile
```

-	Layers:
	-	`sha256:ef9682b66b894cd879de9811734c79cbf164df20091261f805061af74dbc7cb7`  
		Last Modified: Tue, 07 Oct 2025 17:23:37 GMT  
		Size: 191.9 KB (191897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ab9da07a57f0758a4fd10dcdccfd5f46345eea9c284a4676d4ca0ba8555b771`  
		Last Modified: Tue, 07 Oct 2025 17:23:38 GMT  
		Size: 24.6 KB (24554 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; s390x

```console
$ docker pull golang@sha256:a9d7f0dc7f163daf613e2c36345b71834880d8ed68f12dcbc919195a41e39c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.8 MB (86808411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab2f9e903b7ae66026ac537ec349e34f84b33dfbe96c5dfe4853fefab59a9fe`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 06 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 06 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:40ef870b733fb35d27e79770e3e1133cc7c54e14d8c251e61ecccdec69c20e32`  
		Last Modified: Tue, 15 Jul 2025 19:00:19 GMT  
		Size: 3.5 MB (3462100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c0d08c3945d6368d73f257f34ee298e8dee1cce97a4a8bd5b3c35a4f5ab3ee`  
		Last Modified: Mon, 06 Oct 2025 21:15:07 GMT  
		Size: 292.2 KB (292152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b71ba158c27a4a233d289bf79be8c87a013b440db0421d74c9dff9585ea4d5`  
		Last Modified: Mon, 06 Oct 2025 21:06:07 GMT  
		Size: 83.1 MB (83054001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8ab92e39fa2e83c97940ed367640265d9527f15b9af81713066daee42f426e`  
		Last Modified: Mon, 06 Oct 2025 21:15:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:cc1cc30a8517241b020c2352eae6e05531c4f0b747fd7d270179f3bc8eb51f29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.4 KB (216373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e292b1b7de3a5df7b41c4ac0bf55f71ca45ef494f0888182a5ada1e6b9e93047`

```dockerfile
```

-	Layers:
	-	`sha256:eaa06b88d3b329b140701a4c3af031910b12998ba4094291485eb213a3366ff1`  
		Last Modified: Mon, 06 Oct 2025 23:24:36 GMT  
		Size: 191.9 KB (191865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aea765158d04cf376f0175b2d740c60f86f6160afb45d24ac7381a9b9db5f3d`  
		Last Modified: Mon, 06 Oct 2025 23:24:36 GMT  
		Size: 24.5 KB (24508 bytes)  
		MIME: application/vnd.in-toto+json
