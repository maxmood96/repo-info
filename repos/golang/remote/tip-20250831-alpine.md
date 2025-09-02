## `golang:tip-20250831-alpine`

```console
$ docker pull golang@sha256:25935e06062d4ecf246b6925d4aeaf7d3ce41b47a3bd888625703715a7aff67d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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

### `golang:tip-20250831-alpine` - linux; amd64

```console
$ docker pull golang@sha256:de25e633f711c79af641a0b927677b0a72fcf627e26483ec29867fed0f4dbf35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87536633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df2bd90e75e28527e5a588220802018fe6562941bf5f6bdae8bee900eeb675c2`
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
	-	`sha256:9ad57c05d6a015505d9714c638fabbf8d2f856015b238691a6949b24ec31f11c`  
		Last Modified: Tue, 02 Sep 2025 17:25:55 GMT  
		Size: 282.4 KB (282444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3dff0c88890d852f1b6000c60fab1e5090230eba3301a46159a26dd4149cf4`  
		Last Modified: Tue, 02 Sep 2025 17:26:01 GMT  
		Size: 83.5 MB (83454344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca3e2de124dc4d330f004f3611fe69e3331a1d79a8d1529c61aebf80dc59e33`  
		Last Modified: Tue, 02 Sep 2025 17:25:56 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250831-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:256190e2aa19ffcc4c9f7e637343b56610ea70708c75929f120e026e576367c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.7 KB (216665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbd59da94e18a2d6224e299246a45e31f57d7421d4586bb9478a60ab4a7cd6d`

```dockerfile
```

-	Layers:
	-	`sha256:bcf34b893908b268734a3e1dc902581bdf0e0c184ae87f9c637d409f95d21e4d`  
		Last Modified: Tue, 02 Sep 2025 20:23:57 GMT  
		Size: 191.5 KB (191527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2933b76b296b2b9d55661dfe4648766b5c98becd4565ec0ca573d6e3fefa0155`  
		Last Modified: Tue, 02 Sep 2025 20:23:58 GMT  
		Size: 25.1 KB (25138 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250831-alpine` - linux; arm variant v6

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

### `golang:tip-20250831-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:5ef57658fb796298383e5206a8bbfe194f1117fd11c38e3a0ed3d3a789a8135f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f207cefff94cffea4ec4ec4dd9fac3bf4be3e51a6832c25f49688a6bff81ad26`

```dockerfile
```

-	Layers:
	-	`sha256:2a2118a242b4861977bb6d2602f81560affb794c763a02e25360458bfa77287f`  
		Last Modified: Tue, 02 Sep 2025 20:24:01 GMT  
		Size: 25.0 KB (25046 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250831-alpine` - linux; arm variant v7

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

### `golang:tip-20250831-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:c7427622653fce2ec2a4c367c1479e0da9fed5d1ab73b7a1737c68ed584ca6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.8 KB (216811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5055c94466b54c149be429fdc994dab7b8d18dd282ab4200b03bc23fda2c213b`

```dockerfile
```

-	Layers:
	-	`sha256:7fcb1853c25c3e0b970ddf1ac47f5e13ebb5b32a6b58aad5caf21d7fe49eaca4`  
		Last Modified: Tue, 02 Sep 2025 20:24:04 GMT  
		Size: 191.5 KB (191549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f74ae75f71baf4766360475e3aad04ca8996d4250240d9a9358e05db3c37b11`  
		Last Modified: Tue, 02 Sep 2025 20:24:05 GMT  
		Size: 25.3 KB (25262 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250831-alpine` - linux; arm64 variant v8

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

### `golang:tip-20250831-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:c4afc2983b734ca28ad222d1ebd1f0db95221a847d7482dfa2b225b85161a39f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.9 KB (216880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0174144a462031f1821f8f4fffd4548b95c9b90058fa5cb253a2b9a8b9b25581`

```dockerfile
```

-	Layers:
	-	`sha256:137759a935c22feffb37c01d7ce99f628db2a4efdc07dc903519a4abb4069f52`  
		Last Modified: Tue, 02 Sep 2025 20:24:08 GMT  
		Size: 191.6 KB (191583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7393d692ad063613ccc0a41d309042a5ffc485989c27a64ae854925ddcfb4353`  
		Last Modified: Tue, 02 Sep 2025 20:24:09 GMT  
		Size: 25.3 KB (25297 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250831-alpine` - linux; 386

```console
$ docker pull golang@sha256:467cfb3dc7982524869c87350336367fbf5fb2adedf939ec5138234cb7f9ebfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.0 MB (86030862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b43929d90f9762f55ffd905ef85ab74efd00173051d54650ce0d6c89516d943`
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
	-	`sha256:32fd0dff75cb90984bee3de15b0ab6a335241d4c1278b93927a102d84d2c09b1`  
		Last Modified: Tue, 02 Sep 2025 17:27:06 GMT  
		Size: 282.9 KB (282932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc969e7a30537f064821c7c82ed2000b4f696dfb82f12bececa0caf74f9469a`  
		Last Modified: Tue, 02 Sep 2025 17:27:09 GMT  
		Size: 82.1 MB (82132767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f987c2688a4de32d1c7cc9f65ae898ff8a43ad360b3d16b23817db63888a64d7`  
		Last Modified: Tue, 02 Sep 2025 17:27:07 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250831-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:bb76856b397f6d60121d2ea0a1c152a4f21414097f621a204c46bf4b11b5b169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.6 KB (216583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c5f79ee8769094c82b3e87123fe4d11562461f0ebe155d4b159296281a81b17`

```dockerfile
```

-	Layers:
	-	`sha256:05328f89501dbb1970690a238c9745063e1cc7ead95039b8304e8b6987a20212`  
		Last Modified: Tue, 02 Sep 2025 20:24:13 GMT  
		Size: 191.5 KB (191488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a55f13dc0a0760ce69e33aa37c131d86da44a1c7573b1d9889246d268fbaa7e`  
		Last Modified: Tue, 02 Sep 2025 20:24:13 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250831-alpine` - linux; ppc64le

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

### `golang:tip-20250831-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:658ecab00424cea08dfc49d8950466b6d04ab3472c6726441fd32294307803ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 KB (214820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a220235e09f51e4fdf61fab49d19fb7c71fa8e731fa8ed7e68e4058d23c5fb`

```dockerfile
```

-	Layers:
	-	`sha256:70b0834aa1718ab95392a09310c847a61d76d23d6d9af58fafee0cd60b64c932`  
		Last Modified: Tue, 02 Sep 2025 20:24:17 GMT  
		Size: 189.6 KB (189624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82d4505c2f5c94bbe326d3be9f4f958564be14208cad4b7c6590f63392a9a6d9`  
		Last Modified: Tue, 02 Sep 2025 20:24:18 GMT  
		Size: 25.2 KB (25196 bytes)  
		MIME: application/vnd.in-toto+json
