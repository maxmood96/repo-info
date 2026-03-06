## `golang:tip-20260301-alpine`

```console
$ docker pull golang@sha256:a017a3406255e2b4c9d2c25c08b6eaf28513f5e01c3d67f5b962f1e4cd5545f6
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

### `golang:tip-20260301-alpine` - linux; amd64

```console
$ docker pull golang@sha256:d5b25d3c2da68232410f380af4ff37846097a10da654cb683d5b007c286fa809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.8 MB (97761403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5714340e0e013a283ab3d960c616e80823473daf53fa73ba7bc4549406ee636e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 02:01:10 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 02:03:01 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 02:03:01 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 02:03:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 02:03:01 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 02:03:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 02:03:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6dbc279c875b5f4dcaa4a022739a4c63810c5e31c1005edd19efd4b433850d7`  
		Last Modified: Fri, 06 Mar 2026 02:03:18 GMT  
		Size: 296.1 KB (296077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689a8c664b692c42c224e696026ec9ec2afa2556b09a298fb5881d3823f0c6dd`  
		Last Modified: Mon, 02 Mar 2026 22:02:43 GMT  
		Size: 93.6 MB (93603346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0729f5ed354cbd4ac6243cf06604753747b2966af74e580112d1b7fa8d69ae0`  
		Last Modified: Fri, 06 Mar 2026 02:03:18 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260301-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:6e565f8f1e2dea9c1bd5aa9048fa218d1682453379c14230d39549708b6b8992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 KB (220696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53cad0b37bf0722cd532395db07f756002cb208034d55d0ea6d9cd628fbc05b4`

```dockerfile
```

-	Layers:
	-	`sha256:63d95fb30ca5339ee28b641fa36e6f2a30ff81fd955c5cc315605a70bb0b4ee6`  
		Last Modified: Fri, 06 Mar 2026 02:03:18 GMT  
		Size: 195.6 KB (195601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c277c2ff4bfedbe26d57d3b489d43af19dfc97b5f2f75f8e6c24f687a71c4202`  
		Last Modified: Fri, 06 Mar 2026 02:03:17 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260301-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:fff2bd1e7e47bf028e77138a4764b9617122793ee846f609e52bd66f3ac61feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.8 MB (93837837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcfdd48392e4fc282c9dc80301e7da44b82ff07f9bade483c2739c8316098976`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 01:59:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 02:02:16 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 02:02:16 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 02:02:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 02:02:16 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 02:02:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 02:02:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95401a161baa817f60753df76b1db2b8e113c6c233cd65ef651c862aeb213144`  
		Last Modified: Fri, 06 Mar 2026 02:02:31 GMT  
		Size: 297.3 KB (297254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f75482abeb648b9189b3f4696db6444fed715bf37c369ca85b2202c497f7c6`  
		Last Modified: Mon, 02 Mar 2026 22:04:54 GMT  
		Size: 90.0 MB (89970604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85942aa995db329eaf7a4047e785d023e70d38ae76dfe81d2e0975c74b35c4a`  
		Last Modified: Fri, 06 Mar 2026 02:02:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260301-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:ce89bf3229951b1f008b5c62a3b15ca623636d41f2d185e13df16d0739ec0ed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893489728826a6f0757c4d5cea635b34b1a386d18eab180f5334f11c3ecdf39a`

```dockerfile
```

-	Layers:
	-	`sha256:cb1766603ab60973ddc44cb590ea8baeab5686c3921c482d5f1bdc2d72d2c632`  
		Last Modified: Fri, 06 Mar 2026 02:02:31 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260301-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:0fbd32b770ce6452c662bc9c1c12a887293ab36ddec4d501e505c64027e10c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93274747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5307d15933aec3e751a4b1c882a16c6fc11ce36836ad81367ffc30a585dab6e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 02:00:14 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 02:03:06 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 02:03:06 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 02:03:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 02:03:06 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 02:03:09 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 02:03:09 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b35538a47cbc8dc979f6a826d8c01d6a0762ebeae214a7fc706c37bd52149d7`  
		Last Modified: Fri, 06 Mar 2026 02:03:23 GMT  
		Size: 296.2 KB (296202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d47f42e49b5b1824f0c700b4d521593aedaa7278226bf8d2c8c937a0110183`  
		Last Modified: Mon, 02 Mar 2026 22:04:34 GMT  
		Size: 89.7 MB (89696663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e4ee3c66fb363b3a420530f4e9a678fb2fc0971ee31ed77fa8fe21ffdb747f`  
		Last Modified: Fri, 06 Mar 2026 02:03:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260301-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:1240d225979d0193380f52f7877c5d453e6042e1cd20f5249860aa8065e69600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10260ca821584f37b150935f6805db82d55f21e2c58375c9a7a877fb6787b152`

```dockerfile
```

-	Layers:
	-	`sha256:f8199f72e87876fb5119d3b2809164b73ccbcf6fbf9b1817ff745fbb00cdc16c`  
		Last Modified: Fri, 06 Mar 2026 02:03:23 GMT  
		Size: 195.0 KB (194971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26b03739ec0cd711863553ec6ee4f4c813d20985384d09615357783e1d571696`  
		Last Modified: Fri, 06 Mar 2026 02:03:23 GMT  
		Size: 25.2 KB (25223 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260301-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:b877c7efda88693be989188ead51bede2de188990a9d95cab74c9120656d2778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93280910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0cf7ca9107112277614303b48a9f08c98cfbfdbdcde7c7835f41f2b9d20d0a7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 02:04:42 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 02:06:22 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 02:06:22 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 02:06:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 02:06:22 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 02:06:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 02:06:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b3aa006d7b2284c3dfcc0d3ebc261d557b1d033c2bedcff4bdd1f74e4de5d0`  
		Last Modified: Fri, 06 Mar 2026 02:06:40 GMT  
		Size: 298.8 KB (298831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e982fdcb72c3ad1cca7a139b473ea3951042395bd4cf7fbdb4f775c24a9b551`  
		Last Modified: Mon, 02 Mar 2026 22:03:07 GMT  
		Size: 88.8 MB (88784830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555fa88139018c14baece26b6290f848446ce988c64d2edd5643ea58cb0d510f`  
		Last Modified: Fri, 06 Mar 2026 02:06:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260301-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:b5f3674ad6cbd03d8b55bb00ff392719f13be945263764b075d93b7b56e9b60a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.3 KB (220262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96db04320eb5ce0ba673725ffca8a78f4098f7e16210fb655f33658bd99b5e23`

```dockerfile
```

-	Layers:
	-	`sha256:ba1e21da4df8ee07f258cccd28e44d608c18f1fe753e0672da21185f68243b97`  
		Last Modified: Fri, 06 Mar 2026 02:06:40 GMT  
		Size: 195.0 KB (195007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2944f9368a9509988f1f4290e69e7413976fdf38e193911c22108dc8c8bed5fc`  
		Last Modified: Fri, 06 Mar 2026 02:06:40 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260301-alpine` - linux; 386

```console
$ docker pull golang@sha256:bffefa21b7ad5d26bb576b32e87af7ff9aa5c274cbf635ede7321dc6807feca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95432734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e9f27694a459656b1592a25c1a17fa5d03e9b822e31c6a0e87cc87b35233182`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 02:01:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 02:03:24 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 02:03:24 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 02:03:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 02:03:24 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 02:03:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 02:03:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37eb2441629bee4a8b0ab107565f2302a6620d2542e6d1caaa86c290aef3c1a6`  
		Last Modified: Fri, 06 Mar 2026 02:03:40 GMT  
		Size: 296.7 KB (296655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862b2140e9f06d205b6b5af3fcc14f26b13013365f22129c2ff99cb48ee34776`  
		Last Modified: Mon, 02 Mar 2026 22:04:44 GMT  
		Size: 91.4 MB (91448922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34816b75d74c8f02512b518acf015931b2f33bb055c9d1438f7b35e4a0238b87`  
		Last Modified: Fri, 06 Mar 2026 02:03:40 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260301-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:6b65f3791dd7cb9d90494e8ec4f2a8c44013b99f42b018a06d957488bdd5a440
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:360a78acb81569a54511f4792e0bf8bc1a5d801854f0ab30af0b2a3520cac950`

```dockerfile
```

-	Layers:
	-	`sha256:7946b2fe15a84a377b89524370ae233a7dfb75686a7fb3acee67e731cec447ac`  
		Last Modified: Fri, 06 Mar 2026 02:03:40 GMT  
		Size: 195.6 KB (195560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab4e6bd546a6e16d3ba7e05e5a3a2de4dedc100e9e2b0f2edce593b4738b5fd3`  
		Last Modified: Fri, 06 Mar 2026 02:03:40 GMT  
		Size: 25.1 KB (25051 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260301-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:07c610aa23f17aeacc7e29c06976607a74505bd0a5cb7dc0a67eb64b917efc85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94444954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36271c84f0a975d3c2d3757c08e53eb4311cff5ef4d36aaab4986e12f870ffa`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 01:12:22 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 02:02:04 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 02:02:04 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 02:02:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 02:02:04 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 02:06:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 02:06:58 GMT
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
	-	`sha256:abcc3a57b0d1a4c549275152be846eeab1e4bfda9d363982944775991fe15219`  
		Last Modified: Mon, 02 Mar 2026 22:05:31 GMT  
		Size: 90.3 MB (90315888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982c155d3f447cc650e69555a85aa75d5c6a1952f54f1ba2fa5567809576c689`  
		Last Modified: Fri, 06 Mar 2026 02:07:20 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260301-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:dd4874a60b011ef20c9ef8577c6b2d9de3a9e4b1fed800ce4038eaffa9bc33d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9008aa5d1b211d8b03b212b98acd8647353d9f4a1830e8814c5d83dffec3b5`

```dockerfile
```

-	Layers:
	-	`sha256:e76aa4fd9b2b9cd10c6007cbda22a1bb20f0811cade0c8c053fae4923822f87c`  
		Last Modified: Fri, 06 Mar 2026 02:07:20 GMT  
		Size: 195.0 KB (195000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53388c961adfe08adcf4c43e7d99d9a1abf18adebb87f0aad43fcd9fced26a57`  
		Last Modified: Fri, 06 Mar 2026 02:07:20 GMT  
		Size: 25.2 KB (25152 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260301-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:c876dc4c6da23a7bee07a9f76afb401303c54442e86ecd1aed53aabb2a10681c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94671232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81486afe7d6a886501ac8416e771824d53b5f913bb759805408610bc7406587d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:12:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Mar 2026 09:03:40 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Mar 2026 09:03:40 GMT
ENV GOPATH=/go
# Tue, 03 Mar 2026 09:03:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Mar 2026 09:03:40 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 03:21:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 03:21:11 GMT
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
	-	`sha256:7550964df09cbec6e16da50f25098e25826ade610bf4557ad9371e12e9ced3d4`  
		Last Modified: Tue, 03 Mar 2026 09:10:27 GMT  
		Size: 90.8 MB (90789282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b95f9d26c7202c75ed4be62cd3070f05c5fd9fa4ac8d126da86e234cb482bd9`  
		Last Modified: Fri, 06 Mar 2026 03:22:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260301-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:937902ed6c31df6c851f15b0f77815c549d4cdedf612ceb19bd087f9ca8f223b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 KB (220149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b95a0f0d516fe8216fa4e9033b57a3217df19c83fc4fa7dc1adb0491ba8604e`

```dockerfile
```

-	Layers:
	-	`sha256:8cebbd8ddf93a6231a6ea31f7f359533341c7481cfb21dcc6b0dfa4b2d690b06`  
		Last Modified: Fri, 06 Mar 2026 03:22:27 GMT  
		Size: 195.0 KB (194996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8fd5e2a6623cace46ff3fb2eabf896e4f068780093657b881a7687cbabcdd49`  
		Last Modified: Fri, 06 Mar 2026 03:22:27 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260301-alpine` - linux; s390x

```console
$ docker pull golang@sha256:44930bb5272883fe7ea16a9c517fd91a5f1ba2895f6c25394176164d5e071b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.8 MB (96825234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c9c9504bafea1856631466a26fa6c64df6603637b7b184f2a2edd71c547015`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 01:10:35 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 02:01:56 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 02:01:56 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 02:01:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 02:01:56 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 02:02:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 02:02:00 GMT
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
	-	`sha256:bfb2d3098d11b942b930d9b88ef8d2b13e42c10d7ccd12c5e317467f410cfa58`  
		Last Modified: Mon, 02 Mar 2026 22:04:29 GMT  
		Size: 92.8 MB (92802560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a581e947fea70d70ea9acad38f8b3e2021b608be3a8f7518123f2ec2d25e85`  
		Last Modified: Fri, 06 Mar 2026 02:02:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260301-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:3924cb0a464d3f345de69bcf5e735537c86d04cfba5a75b73ddab259a62897fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 KB (219872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3f06330b907592fc2def611bfc61b9eb5ca897132bea4f4fd8c2b99c1b4b8a7`

```dockerfile
```

-	Layers:
	-	`sha256:2358475ae7a168c14eba63d941b0d32a21263cf73b5aecaf2e9e58a71febfa8a`  
		Last Modified: Fri, 06 Mar 2026 02:02:22 GMT  
		Size: 194.9 KB (194950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:294c78c46583049eabb65fda5fd9ec417e2b4fe495338c4f0926668dc8c4e19f`  
		Last Modified: Fri, 06 Mar 2026 02:02:22 GMT  
		Size: 24.9 KB (24922 bytes)  
		MIME: application/vnd.in-toto+json
