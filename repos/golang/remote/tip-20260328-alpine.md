## `golang:tip-20260328-alpine`

```console
$ docker pull golang@sha256:bee2dc2f93ff43ae39cb63744dbf4abbe1cedce21c86c6d421293c769db46d22
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

### `golang:tip-20260328-alpine` - linux; amd64

```console
$ docker pull golang@sha256:443accc17daa067d64d9cf9606104fb0e5b2b18a7cfb017c1c34dcb7cdc81937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98102928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e8d440f4a59e600164cf7ec84bbf30242d9deafcace097412384f92d84b253`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 30 Mar 2026 17:48:30 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 30 Mar 2026 17:47:50 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Mar 2026 17:47:50 GMT
ENV GOPATH=/go
# Mon, 30 Mar 2026 17:47:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 17:47:50 GMT
COPY /target/ / # buildkit
# Mon, 30 Mar 2026 17:50:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Mar 2026 17:50:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f40d6064e1957b1bf3119ce489e4855cd3a387c5f942b2d282862fec500e07`  
		Last Modified: Mon, 30 Mar 2026 17:50:25 GMT  
		Size: 296.1 KB (296079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc94bcc3a046e419ba11b5fddd09ec7514410ba4c53e7ad8d4f5445debcec8a`  
		Last Modified: Mon, 30 Mar 2026 17:48:21 GMT  
		Size: 93.9 MB (93944870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a887ed363f401a562960d14422e34adf137f6168f3ff6d318bcf0dc1405e0dc`  
		Last Modified: Mon, 30 Mar 2026 17:50:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260328-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:c64478c2bc6d26e1f7a8c64a4c7bdd5236099ef5c381154a6e171f883504fb8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 KB (220698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:773cb169f711394eeb1389c49b8515bf37fefe27f2ee1286a1dd35e628f78a6b`

```dockerfile
```

-	Layers:
	-	`sha256:b635663a6f3a31d6ceea1c7206bdc0462d95235137caaeb3000fd84e0e9d4a98`  
		Last Modified: Mon, 30 Mar 2026 17:50:24 GMT  
		Size: 195.6 KB (195603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:decf59592d689ad8c927210cce3d80664c6d954016574475df7e9c00689b35aa`  
		Last Modified: Mon, 30 Mar 2026 17:50:25 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260328-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:f3dc19863a31f63194c7db1126dd54c29f7b167ed2d3a9c192ccda7399d37b46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94216437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062490ba564ca2437441a5b7dd92f25103ad2b3e62012b959ea7cd8b94b54aed`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Mon, 30 Mar 2026 17:46:56 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 30 Mar 2026 17:49:43 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Mar 2026 17:49:43 GMT
ENV GOPATH=/go
# Mon, 30 Mar 2026 17:49:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 17:49:43 GMT
COPY /target/ / # buildkit
# Mon, 30 Mar 2026 17:49:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Mar 2026 17:49:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6273897fdcdb5fe28b0df6738431d45b4cde1aecc82020bd0fc57c7d8792271d`  
		Last Modified: Mon, 30 Mar 2026 17:49:57 GMT  
		Size: 297.3 KB (297257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03647cb457c72e350b07f4610ef3893d0430da67ab19b26b8877e005a07809cf`  
		Last Modified: Mon, 30 Mar 2026 17:49:58 GMT  
		Size: 90.3 MB (90349202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cfd808e4a1a7e14416b9dd754b8315d7744ba6464aed34a4c6480edd043179`  
		Last Modified: Mon, 30 Mar 2026 17:49:57 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260328-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:b37f4de0ae8d11b5c1b6b5bba46ccec37112bc267f734c8d55612702ea622579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c74b164b96a005a87807d954e59767050d5ef802f0acd477a216d91e18d48b16`

```dockerfile
```

-	Layers:
	-	`sha256:8b8a8cf1dc6fb01fdd6a299c038b4653773447e6071d5551891aff16e189271a`  
		Last Modified: Mon, 30 Mar 2026 17:49:57 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260328-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:e7f4cb2cfbefdf054fd070e086b0b3d3c8f5a4ddef274e34185fc8a24a06ed82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93646884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc91db5c27d1b8c69b3c994fe05b04d0cd2dec3199d2807e15ec95001127a6b2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Mon, 30 Mar 2026 17:48:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 30 Mar 2026 17:51:18 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Mar 2026 17:51:18 GMT
ENV GOPATH=/go
# Mon, 30 Mar 2026 17:51:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 17:51:18 GMT
COPY /target/ / # buildkit
# Mon, 30 Mar 2026 17:51:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Mar 2026 17:51:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd5b083958d0d23ea1ac349ab579b0c359d59d3b5f4a9dad03965827ea75149`  
		Last Modified: Mon, 30 Mar 2026 17:51:35 GMT  
		Size: 296.2 KB (296195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10a0142adc6609c1699e104cbb6d09e5264e25e4e76c071ff20b820aebd1914`  
		Last Modified: Mon, 30 Mar 2026 17:51:02 GMT  
		Size: 90.1 MB (90068807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fdab0359730c128c4c4991b29c4b5d49bd135abf94d897c7ce5c200f043d130`  
		Last Modified: Mon, 30 Mar 2026 17:51:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260328-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:7861a32a46fd77e994779456c375a6747e0f579a4a632d5c41b2709afbc1458d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f2aa0b4e9f5f1b683912308b5c0cbf5ff6e86e535f208c8ba5699c7784d7d94`

```dockerfile
```

-	Layers:
	-	`sha256:54c6405131a1c92a3220f49804f879d47d5ca8fce12806e93f35c6fe73b54dbe`  
		Last Modified: Mon, 30 Mar 2026 17:51:35 GMT  
		Size: 195.0 KB (194973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92395182fd993c3b5259beb7657b88895d83c49ea729755be3ad12dbbb8fe8bc`  
		Last Modified: Mon, 30 Mar 2026 17:51:35 GMT  
		Size: 25.2 KB (25223 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260328-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:e67159aa6b57152c9522307c043120bde1957b90e3493bf5dac6c125eef3fa4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93522052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28baa4dcb33a96d80608d7b3db46ac5b0ca321b92f8f915959630a5e5f4868f6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 30 Mar 2026 17:47:48 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 30 Mar 2026 17:49:32 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Mar 2026 17:49:32 GMT
ENV GOPATH=/go
# Mon, 30 Mar 2026 17:49:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 17:49:32 GMT
COPY /target/ / # buildkit
# Mon, 30 Mar 2026 17:49:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Mar 2026 17:49:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5297f56f2b4533277ed4635aeec16b20d6354f52faa3346fecba81dda142311d`  
		Last Modified: Mon, 30 Mar 2026 17:49:49 GMT  
		Size: 298.8 KB (298837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111f485f6c4b82dc9f58e7d75c491e9181371f2ac26e7bd1ac582e69f4e4bb91`  
		Last Modified: Mon, 30 Mar 2026 17:49:51 GMT  
		Size: 89.0 MB (89025966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab43e2d1250ec4e3213a9185b092a7b8fc62cd96df1dda9d0c915f47c03f498`  
		Last Modified: Mon, 30 Mar 2026 17:49:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260328-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:c50322df882b8a24d341bf3d231805715b06c8abef6fb8df555b5d136fbac012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.3 KB (220264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2399fd4d9daedb97f29007a34539a0a0891253444d5e48d6cbae0b684815d5b`

```dockerfile
```

-	Layers:
	-	`sha256:62a95d38d1704ea26b31398c3c96bd1d968c4f1078747f60c6fbd8474602a5b5`  
		Last Modified: Mon, 30 Mar 2026 17:49:49 GMT  
		Size: 195.0 KB (195009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:581d28992e751576b6dea5703dbd0e9bf5f454650b5fde850ecd793e10de9216`  
		Last Modified: Mon, 30 Mar 2026 17:49:49 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260328-alpine` - linux; 386

```console
$ docker pull golang@sha256:8a3832288750f2669caf8e6ba41a18e0e175cbfc00b352e822faca5b52dba519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95753172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a33f710446e18e9fb1fb97b2eb7752e6193f83cc6dd93b5de780400d536539`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Mon, 30 Mar 2026 17:48:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 30 Mar 2026 17:51:02 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Mar 2026 17:51:02 GMT
ENV GOPATH=/go
# Mon, 30 Mar 2026 17:51:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 17:51:02 GMT
COPY /target/ / # buildkit
# Mon, 30 Mar 2026 17:51:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Mar 2026 17:51:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3329305208ff9f88557d18d0cc28a7924a8a6be3f0d9881b85d54273a7a8b2c`  
		Last Modified: Mon, 30 Mar 2026 17:51:19 GMT  
		Size: 296.6 KB (296648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60cd517d6dba9b01cd366f9de5344ce7d7604f0621cccf254c2d056e36d9d4f2`  
		Last Modified: Mon, 30 Mar 2026 17:50:29 GMT  
		Size: 91.8 MB (91769368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d9428f1bd0ad3e3a7c09df4dbf33296a5cae59051094afd3ccb2c2f8b8babf`  
		Last Modified: Mon, 30 Mar 2026 17:51:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260328-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:07d40b6f980582db237ce0ad5dfe52e2053c9b393813a48ce09aeb55d5cba79a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fecc1a93bdde960b0288edd7a2889ddc9643f111380d193a2da1d328c914bfb2`

```dockerfile
```

-	Layers:
	-	`sha256:71d9215099aa904f9c1a9a576b056f60ce7ed0c47a58855d1abc8ffa4eb88adf`  
		Last Modified: Mon, 30 Mar 2026 17:51:19 GMT  
		Size: 195.6 KB (195562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:974a148d6e8896f217b2eadf99dc7c439a821a756478cae1a683b1fef48030cc`  
		Last Modified: Mon, 30 Mar 2026 17:51:19 GMT  
		Size: 25.1 KB (25052 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260328-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:912a00a675a96bb6ec99cebbcfb5e964fb9e045a272d0cd8a701d9d097c5dbd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94861601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c739590039fe6ae9432147fed0a5da7df8ee62763ebfb32b386a735a8a6bf38`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Mon, 30 Mar 2026 17:54:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 30 Mar 2026 17:49:52 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Mar 2026 17:49:52 GMT
ENV GOPATH=/go
# Mon, 30 Mar 2026 17:49:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 17:49:52 GMT
COPY /target/ / # buildkit
# Mon, 30 Mar 2026 17:55:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Mar 2026 17:55:01 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa097d6081c797ea1d2449f426bbf86a030343fa4c35441ab588dce8fa71634`  
		Last Modified: Mon, 30 Mar 2026 17:55:17 GMT  
		Size: 299.3 KB (299269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111969b1f573be958af91f197054c394fc84f73b452627519be6a7f12a1bcd78`  
		Last Modified: Mon, 30 Mar 2026 17:51:17 GMT  
		Size: 90.7 MB (90732531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06393e65407e34cc2553f6243cb081358722054212c0ebc5fe3c7c51f1d616f`  
		Last Modified: Mon, 30 Mar 2026 17:55:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260328-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:902faef462b9fcec962803cc8adaf09ad8b8665e64d83fe1ef17ab4b1a212635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bae859bcd3da761b1fcc568db8d51e33f1c853368b02257793d5bea4babb541`

```dockerfile
```

-	Layers:
	-	`sha256:4817f2f6c6e9680ee61e6a12d8f2da723460cb534d5a3675e98b3eb5efc08f7e`  
		Last Modified: Mon, 30 Mar 2026 17:55:17 GMT  
		Size: 195.0 KB (195002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9db2868f4c44e07d2cf380c04d02155753602b14b4d0253480b0b2d5f3c9ff46`  
		Last Modified: Mon, 30 Mar 2026 17:55:17 GMT  
		Size: 25.2 KB (25152 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260328-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:2d888a04dd2ba893b3c11cb78bb4e9a62319447d93bd93c5e8934ecf571cad48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (94981499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c5efebc9e263702deb259223d0a70848f818e500095dc1bb8103c2e9de727c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 08:51:29 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 30 Mar 2026 18:23:56 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Mar 2026 18:23:56 GMT
ENV GOPATH=/go
# Mon, 30 Mar 2026 18:23:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 18:23:56 GMT
COPY /target/ / # buildkit
# Mon, 30 Mar 2026 19:10:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Mar 2026 19:10:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653a48053074547bb1f8e43c4e508d8a803d45b52e98210c3539d09ceb870090`  
		Last Modified: Tue, 24 Mar 2026 08:53:11 GMT  
		Size: 296.5 KB (296514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6e70b1853c9d42c6bcadfebf9fcf629114d0890e516270d3e090097d9a57f9`  
		Last Modified: Mon, 30 Mar 2026 18:30:56 GMT  
		Size: 91.1 MB (91099540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a8b0cde8845658e47d21a37cc0f374b3a53065a4803236228becc1ab4e1f3b`  
		Last Modified: Mon, 30 Mar 2026 19:11:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260328-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:52928e4ac732c52f20392f96d0e31bb85f50334be9357d21b0e83f2ffdcf61e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476bcb67b748d4d9ca85bf6f033d6dd1962a8020cf3b1865a6af288682a43d9c`

```dockerfile
```

-	Layers:
	-	`sha256:acbca7b20d964230b38885449720df4fa99ee3038f2dade5bab7a6c9bac0cf80`  
		Last Modified: Mon, 30 Mar 2026 19:11:40 GMT  
		Size: 195.0 KB (194998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdb0d3bba34cab60ab1db953cdc3207c067dbd8e05af13f0a3b1c7b0fffd8e53`  
		Last Modified: Mon, 30 Mar 2026 19:11:40 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260328-alpine` - linux; s390x

```console
$ docker pull golang@sha256:240b9eda9947ebb5ce213cd7ec96a91992dd913194084946377de4f16764f3cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97146751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada85c84aef92d1f2d238e9ac86f2e58c1ba86d33284e4cb3ab7f19be8a30af7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Mon, 30 Mar 2026 17:53:11 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 30 Mar 2026 17:53:05 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Mar 2026 17:53:05 GMT
ENV GOPATH=/go
# Mon, 30 Mar 2026 17:53:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 17:53:05 GMT
COPY /target/ / # buildkit
# Mon, 30 Mar 2026 17:53:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Mar 2026 17:53:17 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12560628fb31725cefeaf9fa6c991c793ca88c0725e22f913fb6783ef5b72bd1`  
		Last Modified: Mon, 30 Mar 2026 17:53:59 GMT  
		Size: 297.2 KB (297195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d77473e8e347c240104f79da8f95d36830a796c56bf93ad436d6a5a18785036`  
		Last Modified: Mon, 30 Mar 2026 17:53:56 GMT  
		Size: 93.1 MB (93124064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22abd2e09448046e67f004455696911f1c5697fb41d9334ef4f8f60f102a9d3`  
		Last Modified: Mon, 30 Mar 2026 17:53:58 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260328-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:e66d690ef5ac9c78a0681835d865cbbbdcbe3176db9adc6244ad20845e750efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 KB (220046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde20b9e7dfd31fb72c858f77b94f4c505ba4c83b0b063ffaae72e7bff80bc43`

```dockerfile
```

-	Layers:
	-	`sha256:527bb4c945cba5218fc70e7864b1fa9fbd052863b3c42593e7050bea0cbd2335`  
		Last Modified: Mon, 30 Mar 2026 17:53:58 GMT  
		Size: 195.0 KB (194952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7c3e2d7db29d3c958c29ad7675d6dad2552b0c19775a421b195a961f3ca9e04`  
		Last Modified: Mon, 30 Mar 2026 17:53:58 GMT  
		Size: 25.1 KB (25094 bytes)  
		MIME: application/vnd.in-toto+json
