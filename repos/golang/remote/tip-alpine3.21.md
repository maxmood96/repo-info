## `golang:tip-alpine3.21`

```console
$ docker pull golang@sha256:b74abdd7bfc2a36d30f672fef8e361776fbf09b559535fc281bd80639c238010
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
$ docker pull golang@sha256:f1188ac72c9182f10bb1296bdeca4d0a0a9d7ce9c31d6c79346bbd33d38f0dbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87054388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1646be9a387646c44671c3bc81198def6b833a16e8994ce6f1b3d94628282ed5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 18 Aug 2025 05:23:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
ENV GOTOOLCHAIN=local
# Mon, 18 Aug 2025 05:23:18 GMT
ENV GOPATH=/go
# Mon, 18 Aug 2025 05:23:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Aug 2025 05:23:18 GMT
COPY /target/ / # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67451f0d3052efc836fb25811a3eab8f29cc80da2e49b70f79b9fc8824f4f6e3`  
		Last Modified: Mon, 18 Aug 2025 18:22:09 GMT  
		Size: 282.4 KB (282432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c981e030468965854d1b7da64b902a546cf410e421543877a0dbcd1eb3b5506d`  
		Last Modified: Mon, 18 Aug 2025 19:09:02 GMT  
		Size: 83.1 MB (83134228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0eb95d100b3a1d10f5107f0faa7620ab444ca3ae29d5f5245aecac0057733ca`  
		Last Modified: Mon, 18 Aug 2025 18:22:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:61c45019d968f70f609668a076d54e7aa1f9184d289161286ec11e75502f8dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.6 KB (214627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2e49efd5042ea79391f5e28a6e30b88bca74f423228e0ad55cbab0fb63daa0`

```dockerfile
```

-	Layers:
	-	`sha256:da5eb3fb4fa873db67305eada240d9e9704f8f695a9efdbc55b54f1828246c47`  
		Last Modified: Mon, 18 Aug 2025 20:23:54 GMT  
		Size: 190.1 KB (190120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6093861fb6108d8dad3a0f89f5f67c3206a3732abc9a366c45a53624b818670`  
		Last Modified: Mon, 18 Aug 2025 20:23:55 GMT  
		Size: 24.5 KB (24507 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v6

```console
$ docker pull golang@sha256:164b8dda67380637cb26514d5dd231565fbcc95bcda3107e4e045f4d3016c714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.0 MB (84042934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cfecfd1c9b322a307c9c59b690fa1108bd7a91405e56a68b4eb929e3b0be754`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 18 Aug 2025 05:23:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
ENV GOTOOLCHAIN=local
# Mon, 18 Aug 2025 05:23:18 GMT
ENV GOPATH=/go
# Mon, 18 Aug 2025 05:23:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Aug 2025 05:23:18 GMT
COPY /target/ / # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ca0c331561564c536ffa9246944bb50ac21d3fb11fe66c38baad97fdd1f05719`  
		Last Modified: Tue, 15 Jul 2025 18:59:41 GMT  
		Size: 3.4 MB (3363814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4a214d6543aa5b234ca6b16aa4d8e27cbc22cad32bed5ef48890ed7409c406`  
		Last Modified: Tue, 15 Jul 2025 22:48:38 GMT  
		Size: 283.3 KB (283275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37585a3cefa6eac4cd3e186fb9d4cb0cec0d9885ec6592350e2308f3ede04143`  
		Last Modified: Mon, 18 Aug 2025 18:20:58 GMT  
		Size: 80.4 MB (80395687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4870b70c70a9bbecec5f113fbc31b8a581be8e6cd85ca4771cff28b37c49a6b4`  
		Last Modified: Mon, 18 Aug 2025 18:24:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:a69ca321e1c24af652a82e6ae1e5858c9f4a2a21b5a5d17a074a09176c65c7c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fb64155710047f0401ed917ebea114de22f95bc76868d8969085adc9ab17844`

```dockerfile
```

-	Layers:
	-	`sha256:800faaa08f37616b3d58a4657e05563f22fb930d676bf18ba7b8ded01a0b0292`  
		Last Modified: Mon, 18 Aug 2025 20:23:59 GMT  
		Size: 24.4 KB (24401 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v7

```console
$ docker pull golang@sha256:82038263a44335ec1d57acada417e626837fcf6587a3956aec12d6933fb5f9d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83459934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18e905e533bbd733c9174653edd44fb7f2900eba1ca2a4725812a860d6f6264`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 11 Aug 2025 05:23:23 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 11 Aug 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 Aug 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a96f521d793eec1dcb2b825985eb01c309edb500ebd753a2f84cb9430f05802f`  
		Last Modified: Tue, 15 Jul 2025 18:59:46 GMT  
		Size: 3.1 MB (3096871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce1ad2f4fb08bb90f837004e5025b472d374435573f34a4ee7d7287172cfa5e`  
		Last Modified: Tue, 15 Jul 2025 22:36:22 GMT  
		Size: 282.5 KB (282462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331d10df13da6c65403fe5e3b6a9cc280dde2bb564435b287f2b85119c986cc8`  
		Last Modified: Tue, 12 Aug 2025 19:00:44 GMT  
		Size: 80.1 MB (80080443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda420816aaa74edc1dda2990da1e4dda01881f7c03d17f2ece4affe2a81735a`  
		Last Modified: Tue, 12 Aug 2025 18:08:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:a195415a45c145b9e027432b25f7f63a2fd1d897ef01e1b052e23549678663ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.7 KB (214742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:572a57812c7662883a8c24eb33b1d36ce29d63759712ad2328056b3273a7ad9b`

```dockerfile
```

-	Layers:
	-	`sha256:fe79c3a3ce1c4ee6acf68794095674993b27154726830c451bc6a69c06b2b53d`  
		Last Modified: Thu, 14 Aug 2025 08:23:51 GMT  
		Size: 190.1 KB (190126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b0cb300eaaa232de8b2f0914dc118388a9202993d951c5ee17dfcf0025a4b5b`  
		Last Modified: Thu, 14 Aug 2025 08:23:52 GMT  
		Size: 24.6 KB (24616 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:ed1a10566bb6eef3cad232d2550af4d5701e0760b6ba27cce542bb17db5e4081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83277194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58b4d2eeca7f5df44feaec3df462bbcbd6f778870d130136d26fc9043dacbd1e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 11 Aug 2025 05:23:23 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 11 Aug 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 Aug 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df80bb7562bd7e03fda0615c89df2976c21bcf7fd34bd1bfa24010374df289e7`  
		Last Modified: Mon, 28 Jul 2025 20:57:12 GMT  
		Size: 284.7 KB (284686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87b7cf68665eac7cfd64f5bb944a8b17de913d4de7e1d26ec5a73f422afb207`  
		Last Modified: Tue, 12 Aug 2025 22:36:24 GMT  
		Size: 79.0 MB (79005413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea9500d5659433fb46eee84660f0e23470b8994130ae93b8c80a5b69a18cf2a`  
		Last Modified: Tue, 12 Aug 2025 22:38:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:3fed1042d323cd681b9be2460c62cbf47e469eda9838357903b223d508c32c04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 KB (214796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddac4146f17bb8926f9a4b429dd51f4173e65666e4a12c6e0fac5cb979f2d5dd`

```dockerfile
```

-	Layers:
	-	`sha256:d6c18d665b6baaf502f7caa972051f0a738e2518c218f108762b16cd320aa10d`  
		Last Modified: Thu, 14 Aug 2025 05:24:19 GMT  
		Size: 190.2 KB (190152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ab8b776c3f0d608bbc8bd77cc32cf48471e2d1cf98caf42b6edbfce2691dfad`  
		Last Modified: Thu, 14 Aug 2025 05:24:20 GMT  
		Size: 24.6 KB (24644 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; 386

```console
$ docker pull golang@sha256:7996ee6b609938e4930c09e647dd4a57067061f3f1a13f9a4927eae42c3057b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 MB (85502867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ffb8da692ff893dc00b98612f4c2c2e7fdfb79dca3a8c3eb3b417fa5b7407b0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 18 Aug 2025 05:23:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
ENV GOTOOLCHAIN=local
# Mon, 18 Aug 2025 05:23:18 GMT
ENV GOPATH=/go
# Mon, 18 Aug 2025 05:23:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Aug 2025 05:23:18 GMT
COPY /target/ / # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:47ad0adcb4aa253584437783c542bfbd2276c07a7a0b7487bb26f9b2e80cba73`  
		Last Modified: Tue, 15 Jul 2025 19:04:30 GMT  
		Size: 3.5 MB (3460726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662a00ecc97b1a33729df23f488412ad861aa21dee712be287aab515915c154f`  
		Last Modified: Mon, 18 Aug 2025 18:22:17 GMT  
		Size: 282.9 KB (282888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82670d3acf9adce43c089b894a11312540a785c816af45b90edbb17d606892e6`  
		Last Modified: Mon, 18 Aug 2025 19:08:00 GMT  
		Size: 81.8 MB (81759095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a3a60561f24bcbccea5857232a07b403dc28d67473c7eea443f58518965a10`  
		Last Modified: Mon, 18 Aug 2025 18:22:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:0008bdcd494cbca1eac9f18ae9dd28c036a5add293e2ef2fb7b323413d31efd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.6 KB (214566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73382a132212e96d43a3282ec7826eb148085dcd33b0aee693fa6cd8bb317e6`

```dockerfile
```

-	Layers:
	-	`sha256:2a8b900f839a9dfa42ad9d09216a2cf91a2df3f5be24d3dfe6b6f58d51d5be0a`  
		Last Modified: Mon, 18 Aug 2025 20:24:03 GMT  
		Size: 190.1 KB (190091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c15af29033c9f907d00f1a75fd8364d3e364d7515c534f3b1ff08935cf1af04d`  
		Last Modified: Mon, 18 Aug 2025 20:24:04 GMT  
		Size: 24.5 KB (24475 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; ppc64le

```console
$ docker pull golang@sha256:65e4622c2d454d3890017b48d350b7676637d87aec28a1f34a54a4c1fc8115f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84257379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:660d94f872af25a0f04efa158f5fadc6f89528d2fbeff0bfa88eddf9de7b8c8f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 11 Aug 2025 05:23:23 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 11 Aug 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 Aug 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bf93837577694839723892fa29fd11013552ac59944071e2341ac6d6d9876d29`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.6 MB (3569125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4292e2d4d9d8706c1de48009e1d142646f4d2a8bd05fff7fc3f70c75ef02d1c0`  
		Last Modified: Tue, 15 Jul 2025 22:37:55 GMT  
		Size: 285.1 KB (285061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d949d12b56c803641dc1ee823fe0b4254f92598b51ea3dd4b12bbfc422e9b7`  
		Last Modified: Tue, 12 Aug 2025 23:22:22 GMT  
		Size: 80.4 MB (80403035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b02f8d1ff57214caeb1d39b5669a8862a991d4ffb5476fb79df48c4e6dd09de`  
		Last Modified: Tue, 12 Aug 2025 23:25:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:da15affc33d6c97b7406589a78dedf9626f5ddb034f52317e95ace6d956d70aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.8 KB (212759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:700d62b717565c39c086184a9973ae9f6a1a6ea2c59edeff9a1e0126c52fb100`

```dockerfile
```

-	Layers:
	-	`sha256:e8e18d7754a624e918db253ceddbb30b677b707b44083e38cd4af23a17711958`  
		Last Modified: Thu, 14 Aug 2025 08:23:59 GMT  
		Size: 188.2 KB (188205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b040e8126730e5712b1653eaa5589cd56be3097c93fca6d6da5df21e75f6c87`  
		Last Modified: Thu, 14 Aug 2025 08:24:00 GMT  
		Size: 24.6 KB (24554 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; riscv64

```console
$ docker pull golang@sha256:c9ce46e753306d28597e549e8abc8248436cac041c0e19b88302d94bc4ddcec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84099249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7091a039eb61bf19470bd4c8b899e97200c599e86b9f093cb6a5ed9db2db5a91`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 11 Aug 2025 05:23:23 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 11 Aug 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 11 Aug 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 Aug 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 11 Aug 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0630095d87a868716a00796c50906a7361ad7a790e9e9151e3bb310f8846f6`  
		Last Modified: Thu, 17 Jul 2025 15:36:08 GMT  
		Size: 282.8 KB (282751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913c1159826bb23e5196b06096f2b66ad808c31d84200f35d658ee413af6cd93`  
		Last Modified: Tue, 12 Aug 2025 21:35:10 GMT  
		Size: 80.5 MB (80467250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42fd43905e617b58925844dac142f42a592669d7d5e27a8cf9531da1258a2976`  
		Last Modified: Mon, 18 Aug 2025 11:07:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:48b6e74896c2830f5c9030d5bd74e499f8edf086550cc8dd70ac7902c4400f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.8 KB (212755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35c32817f1eb0ed55e448dd2a76f8ff95c2fb57f5e13e2f4fd454468c1a67ee`

```dockerfile
```

-	Layers:
	-	`sha256:9dfa0863166ac8e13ba0d167ed30d0175347f709d2ed27e02e62bdf1559e94e6`  
		Last Modified: Mon, 18 Aug 2025 17:57:11 GMT  
		Size: 188.2 KB (188201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:741b44cbe007cd9e41e78d63adaa3a07b21de43ba6799b5fbdadf388615e6707`  
		Last Modified: Mon, 18 Aug 2025 17:57:11 GMT  
		Size: 24.6 KB (24554 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; s390x

```console
$ docker pull golang@sha256:e0857f77994851bdd3f1d04f5e23a3c76598415677c0eef7628cc309036bf527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85443085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4469fc87133732b0b1546d6abf83f8a93e69d6116fcae8e304e157492cc8c53d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Mon, 18 Aug 2025 05:23:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
ENV GOTOOLCHAIN=local
# Mon, 18 Aug 2025 05:23:18 GMT
ENV GOPATH=/go
# Mon, 18 Aug 2025 05:23:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Aug 2025 05:23:18 GMT
COPY /target/ / # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 18 Aug 2025 05:23:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:40ef870b733fb35d27e79770e3e1133cc7c54e14d8c251e61ecccdec69c20e32`  
		Last Modified: Tue, 15 Jul 2025 19:00:19 GMT  
		Size: 3.5 MB (3462100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7c2184ed1d560f97be7198cd6f9baa12de8a0aff6bbb89596217c942ed2797`  
		Last Modified: Tue, 15 Jul 2025 22:45:47 GMT  
		Size: 283.4 KB (283425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3316bff964f9f759871a9216a703323b51e64d4b58eb53b6a858e7831c8cd357`  
		Last Modified: Mon, 18 Aug 2025 18:40:20 GMT  
		Size: 81.7 MB (81697402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3c132e39d3397d3dc38e546238addfb063bc0475396a771b0b09049c76f199`  
		Last Modified: Mon, 18 Aug 2025 18:56:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:3f15b0369e163a26ac110b0d08b67f0f7cc34536a541aa4b0d36c6b29c1b35e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.7 KB (212677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f6b9f4dc94af129bec297cdd7c1874dbe53d349101645b697650d062adb236`

```dockerfile
```

-	Layers:
	-	`sha256:8729e5a227474cc4edcbe0884bb8256104b7bc835337f695f9d88679c2ec29a8`  
		Last Modified: Mon, 18 Aug 2025 20:24:07 GMT  
		Size: 188.2 KB (188169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48971d1e17e9e071d234d7158dc89d92c861f032444ebba5b6175cea744bf119`  
		Last Modified: Mon, 18 Aug 2025 20:24:08 GMT  
		Size: 24.5 KB (24508 bytes)  
		MIME: application/vnd.in-toto+json
