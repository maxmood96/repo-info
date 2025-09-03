## `golang:tip-alpine3.22`

```console
$ docker pull golang@sha256:cd1bf50f2781c1d3a2992addbb86ee295916a7883e427e24f917fd313fc8ffe9
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
$ docker pull golang@sha256:e10f718bc29df595a3fa2880708ede6b02a10742e309411e96cdf953ccb94eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87536639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f9d37ce79910127a229f10749deea932fa1ccb7032d06c12fbec52b5cb56f8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 01 Sep 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 01 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd52ecb9eb60990b270cb57df0d8dce4447a9598c06530918dc9073bb3a1a76`  
		Last Modified: Wed, 03 Sep 2025 19:07:13 GMT  
		Size: 282.4 KB (282448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3dff0c88890d852f1b6000c60fab1e5090230eba3301a46159a26dd4149cf4`  
		Last Modified: Tue, 02 Sep 2025 17:26:01 GMT  
		Size: 83.5 MB (83454344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a8371c802de80bbf0f1f8991659e10236e5923c8036d4483025cec007570b2`  
		Last Modified: Wed, 03 Sep 2025 19:07:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:2f2771c368ea1200f561e575938ad385e28b2c95ff80b12d181aee189aa5ace8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.7 KB (216664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5d113a1883613d93cec50c73a677060aaac3db8b36af4a0d3c12eace8070d13`

```dockerfile
```

-	Layers:
	-	`sha256:c0c999a869a476c78712dc8933761a0dce72b008640e34dbd9ab3747bc172182`  
		Last Modified: Wed, 03 Sep 2025 20:23:58 GMT  
		Size: 191.5 KB (191527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:748c55cc0833eb73d6ea7024b7c5631c85a2f63277c4699b3e09dce861bbcbbc`  
		Last Modified: Wed, 03 Sep 2025 20:23:59 GMT  
		Size: 25.1 KB (25137 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v6

```console
$ docker pull golang@sha256:e0756f482a301824d9d684f282a60c564ec722dcd85d0486615c77957ab0ef73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84518811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee511813c8f85ab15fd257ad9b418bd772694d9f4c5d355be86ed627d707115`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 01 Sep 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 01 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f95cea4c439fb384d1bd6927f75cd3bde82d7a5909bb38cec72c9923ca463a`  
		Last Modified: Tue, 15 Jul 2025 22:55:40 GMT  
		Size: 283.3 KB (283329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4f8085d3112f423ea1896156056d65bf494bfe035c7f45a8b926d0806a425b`  
		Last Modified: Tue, 02 Sep 2025 17:25:15 GMT  
		Size: 80.7 MB (80734416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4446b25b29b06b2fc97279cbbd6267440a7f6aee721c1f44a0eca87a2c49df16`  
		Last Modified: Tue, 02 Sep 2025 17:25:09 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:0e9df45660172db215c2c7abc00cf2ea4d7f08ae3f570ea08f38de3702f27d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55bf0a7cb7f094485f8220faa30eeeae1730ed46beea33041b31af9d947d1426`

```dockerfile
```

-	Layers:
	-	`sha256:c8b0d198b3f77182c2b69d3deb547258bcb31c6ff66901edb23e352fba2c7556`  
		Last Modified: Wed, 03 Sep 2025 20:24:02 GMT  
		Size: 25.0 KB (25047 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v7

```console
$ docker pull golang@sha256:8b5f40be24ce53c9ead1b6ebb65a8ed63b613446402db51527bee4c090a53aab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.0 MB (84013970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:708d939e450b0418f2ea9eda0c9e26b5f6e7610e04ea609d4da1e13231bd0c04`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 01 Sep 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 01 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d1c7cd6f49363bcd6156bb689087c0a4e1624bb6497290e03e589310895c3e`  
		Last Modified: Tue, 15 Jul 2025 23:00:53 GMT  
		Size: 282.5 KB (282485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8183d7d02c47a9b085b3d0bc6d67309b7fa4b7ef97cac1694dc0b5ea8b6ce9c`  
		Last Modified: Tue, 02 Sep 2025 17:26:14 GMT  
		Size: 80.5 MB (80512289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba87bac453220f2e79296ba55b884f58ca354e66a820e73f35a7ee1a9c4e118`  
		Last Modified: Tue, 02 Sep 2025 17:32:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:12abfe4e7f93ef3ed612c6f67c8f58d217bc6e606e9a254b490c623120bfd311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.8 KB (216811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8b190d7322405cd0c85a9d0fe50801344c11616e30f9cf2ab0e8a75b2c8a049`

```dockerfile
```

-	Layers:
	-	`sha256:133413a42d959d8ae468a161b3a0fab97eed36c0cea380db3547f8a66316e237`  
		Last Modified: Wed, 03 Sep 2025 20:24:06 GMT  
		Size: 191.5 KB (191549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:419077c4158cd7fd41fe308d0592f5da628d4e7864763306bab0abbfcfe07655`  
		Last Modified: Wed, 03 Sep 2025 20:24:07 GMT  
		Size: 25.3 KB (25262 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:5ad0a3d3ee9c67c68af590f1a79559def9292fe52739185ce1c7b9226bb40a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83879077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e4a158102989352f46a8b4ed881cddee3990e5567721d4e3d143d51f0f45ef9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 01 Sep 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 01 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21357df949f743a56d3417cb15486b8a5579e1b74b558f43b89f72158c8010f`  
		Last Modified: Tue, 02 Sep 2025 17:28:59 GMT  
		Size: 284.7 KB (284705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948ccd09d5c498d3bdd3015babafec64e8e01106fe6a739f268b131403fa7cbb`  
		Last Modified: Tue, 02 Sep 2025 17:24:20 GMT  
		Size: 79.5 MB (79463464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c27de6762ec6e9751df491f3adc0b399fb062458f6a695574cff548c5e31b95`  
		Last Modified: Tue, 02 Sep 2025 17:28:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:fb1913b5c3b2001da1ef33f38d1a3b6ec2255fe1509f3dd846bf6bed9c562b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.9 KB (216881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62fdde1c5b58ef37cafc0dce67411d0676a44c1a1bab03d6f4541c227f011a2a`

```dockerfile
```

-	Layers:
	-	`sha256:bd955ef1e9429189ffa1c06bd08bf27472c047b91990e24f17f237ca693b4814`  
		Last Modified: Wed, 03 Sep 2025 20:24:10 GMT  
		Size: 191.6 KB (191583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:300030301c99c9ce564d047e0ab261bf6794fb7974bb825bc428461f5a19d687`  
		Last Modified: Wed, 03 Sep 2025 20:24:11 GMT  
		Size: 25.3 KB (25298 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:6c812fab7dd99e02cba75760d215bcf908a3baf3ea41ccb6389cd1f28ac682ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.0 MB (86030866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05fc8d433d834906837ea26bb1b814663539ee04488b3c8ee43f4a309fddce56`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 01 Sep 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 01 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf975eb02760d6c50085b8761bac087eafa72ae23fe840cf1693dff9121af573`  
		Last Modified: Wed, 03 Sep 2025 19:08:02 GMT  
		Size: 282.9 KB (282935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc969e7a30537f064821c7c82ed2000b4f696dfb82f12bececa0caf74f9469a`  
		Last Modified: Tue, 02 Sep 2025 17:27:09 GMT  
		Size: 82.1 MB (82132767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78f52e7bd16b9510ac286bff8a2b6af0bcef73e63ec620ddad1b3adba566129`  
		Last Modified: Wed, 03 Sep 2025 19:08:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:f0a747763282563fef56f018ee639514501e4ccc6207bf79850a4d17f4b30a26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.6 KB (216583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e58582aeaadaddc2a941e5fc90139e5e127295a4f9b3ca08eef42eead5ff71e`

```dockerfile
```

-	Layers:
	-	`sha256:55915051cb11c9468dad5b24bc5c4a6cc98147f11b758e6d3e1c9fd7b6e93710`  
		Last Modified: Wed, 03 Sep 2025 20:24:15 GMT  
		Size: 191.5 KB (191488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f481ae54e6a56df14f4c3461b39eb2a90e84eea846bd6dc7f2cf7fa17e02956`  
		Last Modified: Wed, 03 Sep 2025 20:24:16 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; ppc64le

```console
$ docker pull golang@sha256:43da9e4eda68b38306e899ed92f4f626e2187feaa929c6d0939a9e49f53adefe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.8 MB (84828307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61afb74d9eed1731a50abd3cc6da0862f8bac3ddfe982149510c77fecacfbcca`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 01 Sep 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 01 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8093a8784e85737b54c7bd288e58eb1c4d919cf932185be9835fe0acd194ad05`  
		Last Modified: Tue, 02 Sep 2025 17:37:11 GMT  
		Size: 285.1 KB (285121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65adef97a585f4d6f34375efc6b453ef50bc737c051ef6eb9403cedd2e831eb9`  
		Last Modified: Tue, 02 Sep 2025 17:28:09 GMT  
		Size: 80.8 MB (80815917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6c32a48d93963a4d27813669fdbea9c34f26e45cd91fbaa9d96c210dbed8a1`  
		Last Modified: Tue, 02 Sep 2025 17:37:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:7e151042de03954acd66d71dce8afa6481b40413e297dc28b494925bb236acc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 KB (214820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e14dcf6c30366f933c342e1d899cc1dfb8839924cc77cde3fa8054eefbedab`

```dockerfile
```

-	Layers:
	-	`sha256:b4a463f518e211f862ba60f08a5395bbb13e72a2235414789abf0f3f130fb36b`  
		Last Modified: Wed, 03 Sep 2025 20:24:20 GMT  
		Size: 189.6 KB (189624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbc0bbb4276e97da55c00b023a3aaa23ee2fb0539e1de4409c5330021dbfaeec`  
		Last Modified: Wed, 03 Sep 2025 20:24:20 GMT  
		Size: 25.2 KB (25196 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:e22af9fc5cbd5f37886f4502f6da91d16771df25bc0aedf9d17572b41cd1d7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84686874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ee6c366a39cb66afc19a0cad905311eca4c532943bb8771efa36634298ff00`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 01 Sep 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 01 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e09396f9703679f1457da8ea8533cdf5f2a459c8f9efa4664152e578880b25`  
		Last Modified: Mon, 21 Jul 2025 22:46:21 GMT  
		Size: 282.8 KB (282780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293eb689539c18522b5644ece27c44567aa0a4ab5ae7b74edd76c1cea9f0f71c`  
		Last Modified: Wed, 03 Sep 2025 05:13:46 GMT  
		Size: 80.9 MB (80891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7afa004129fb15f859e90a6e4fa3f104a09530c1c655b24f9022987086dc9c`  
		Last Modified: Wed, 03 Sep 2025 05:55:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:d3a20d682a5d5b95f1961ec674eb08637c278c7157585829f0e5b5323e765563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 KB (214816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a169035a0aa577689ac9c8a10c6094e6c942a28ddb5ec663f6f3891de1b9ed`

```dockerfile
```

-	Layers:
	-	`sha256:0f3e9194f1db017e7d8cbf17bd2e9172670e4b22f409ae800b172dcd6d9a0d3e`  
		Last Modified: Wed, 03 Sep 2025 08:23:34 GMT  
		Size: 189.6 KB (189620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3488f7f26104ac32c28e0ff47ea558f81f3ab4f45d3c52bd6c561b4bae7d677d`  
		Last Modified: Wed, 03 Sep 2025 08:23:35 GMT  
		Size: 25.2 KB (25196 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; s390x

```console
$ docker pull golang@sha256:43179f0451810b916d4a0e1afabf734770cf117e307a987835a4dfbfdf588731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85613923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c3e47109ce94f595ec10b72a9635408f2d01cf02ab4a7bf6139b7bb00ce76ac`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 25 Aug 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 25 Aug 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 25 Aug 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Aug 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 25 Aug 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef24d483efe8f2b1053cb578dbafbffab2dfd6a644764474184fb805fc872f3`  
		Last Modified: Mon, 28 Jul 2025 20:31:35 GMT  
		Size: 283.5 KB (283470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4bb0635d2e248956f88a4462ee973445c0bd3979670795027980550063343c5`  
		Last Modified: Mon, 25 Aug 2025 21:46:03 GMT  
		Size: 81.7 MB (81685324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26b5e15cea26bfba3d806b305de0e048ed58f73c6c7fbfccf118149635cc72a`  
		Last Modified: Mon, 25 Aug 2025 21:52:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:dc50af86fc91919aad11b3f5166f550f61e7c5b4ac48d62baf5bde048ba0b2d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.7 KB (214714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3df7b02b1cb904c52424d2f577ea0dff59654d22d5e02edc4a57445fb06b988`

```dockerfile
```

-	Layers:
	-	`sha256:aa8b03892fb0e78eee48e31ffa68a60c8cadc32553474c81197e2e73786f2721`  
		Last Modified: Mon, 25 Aug 2025 23:24:22 GMT  
		Size: 189.6 KB (189576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2662e12a48a27fd6fe7002c85b493cfb4f5be545e91631b9065ee793dceffddf`  
		Last Modified: Mon, 25 Aug 2025 23:24:23 GMT  
		Size: 25.1 KB (25138 bytes)  
		MIME: application/vnd.in-toto+json
