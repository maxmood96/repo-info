## `golang:tip-alpine`

```console
$ docker pull golang@sha256:13435a0982d32426aa90213780e1bcaa6d901efbd9ec884af9ed8d502db737a1
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
$ docker pull golang@sha256:9acd68a5bec4bcaaf0f716874d3a07b70a58a6512ba92983507a6dd61abd027b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.2 MB (106196217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fddf3ba903e9171348fb5695f83f4a11227254a50c7e987b3f8533c4301761b2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 01:16:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Jun 2026 01:18:43 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jun 2026 01:18:43 GMT
ENV GOPATH=/go
# Tue, 16 Jun 2026 01:18:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 01:18:43 GMT
COPY /target/ / # buildkit
# Tue, 16 Jun 2026 01:18:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jun 2026 01:18:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b60d159af7073a672af1ec80ec81772ee27543a5d4c161a7cd9158b140ada8e`  
		Last Modified: Tue, 16 Jun 2026 01:18:59 GMT  
		Size: 245.1 KB (245059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f299e0e3bd5e6acb73b7c4b5cab40f1e2dfe3ddb2a4bbbe05ceba99d84f0fdf`  
		Last Modified: Mon, 15 Jun 2026 23:29:20 GMT  
		Size: 102.1 MB (102104608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039375a4b5029d23ef70e01ab297379d83534e11543afb948b016e3dcfa4d690`  
		Last Modified: Tue, 16 Jun 2026 01:18:59 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:9ff74320e50091824d3206128bad8c199f0ec5a3dae440e3be79c9be664e7cac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.9 KB (201851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219f0ce3f4f10f39295a5c957ee60bd5a41732fbca53cf44d71e10f9364ac46a`

```dockerfile
```

-	Layers:
	-	`sha256:d8e95f9622d1018026823aed035c58ea5b0b14dd0d58ac8dba37a7aa3e96687c`  
		Last Modified: Tue, 16 Jun 2026 01:18:59 GMT  
		Size: 176.8 KB (176752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93dad3abe4644f95f27675b777bde225eb30d7ae0044967d55090a3bc63751cc`  
		Last Modified: Tue, 16 Jun 2026 01:18:59 GMT  
		Size: 25.1 KB (25099 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:0a567d56aaa64abe2ae36dc3ca7c71b2ca494670a9a7b6bc654184a65851a59d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101943000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1051371a81246f42d7828d69ca14b7f48209b2fe6c29eab36958dd5f52793868`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 01:20:09 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Jun 2026 01:23:18 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jun 2026 01:23:18 GMT
ENV GOPATH=/go
# Tue, 16 Jun 2026 01:23:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 01:23:18 GMT
COPY /target/ / # buildkit
# Tue, 16 Jun 2026 01:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jun 2026 01:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97b393dc337e7421470f49991132516732449659b16261e80fa2385df2c13ac`  
		Last Modified: Tue, 16 Jun 2026 01:23:33 GMT  
		Size: 246.1 KB (246132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7348edabd82bf14cb4cd059795ea4686f60d5bc93e843f47bf9e71da8ef5c5`  
		Last Modified: Mon, 15 Jun 2026 23:25:28 GMT  
		Size: 98.1 MB (98143261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb035768fe5c5889b025bac8be48b304e29edc2e425454f285fbaaa2ccb600e4`  
		Last Modified: Tue, 16 Jun 2026 01:23:33 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:b8d724eaccdac9aec385732b5755e2911a0bee7b021656f4ba8eb48b994c8f37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90485e499cc1834e844379376eb3dd4059f2d6fed49705f617f60bee551ec35`

```dockerfile
```

-	Layers:
	-	`sha256:b15229e8d725abd1f3757de5eabfefc1d74744c451af78a4307b37aa09ce1c68`  
		Last Modified: Tue, 16 Jun 2026 01:23:33 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:540b9f409ca32ae4423185b46b719dc833d197b94b06bf9d632cce822108dc14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101342064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0bfb71e1c596d162e7d20dc4c57a07c3c2103338253bc4aa10ee8b6376be308`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 01:20:02 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Jun 2026 01:23:09 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jun 2026 01:23:09 GMT
ENV GOPATH=/go
# Tue, 16 Jun 2026 01:23:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 01:23:09 GMT
COPY /target/ / # buildkit
# Tue, 16 Jun 2026 01:23:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jun 2026 01:23:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0e4810c67544068866393b8bb43fd13e4b57ea16d4a09af99e36937f483779`  
		Last Modified: Tue, 16 Jun 2026 01:23:27 GMT  
		Size: 245.1 KB (245111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f3afb2b46cd31bb80c259a8638a98ac035a8bd800ea0d4d4395dd90003ea00`  
		Last Modified: Mon, 15 Jun 2026 23:27:30 GMT  
		Size: 97.8 MB (97836180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417e68d799464284a3b26cf392b4859046b8f1df74c45ee0faa72f0f7439c9b4`  
		Last Modified: Tue, 16 Jun 2026 01:23:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:2a67935035ba13578e9f5562e7dd5fbcd07cadc072f5b7d8d0f415e2bb1f5293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 KB (201345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c76b251f767ed02aee4c48b3f55fced7753d248955beadde3ebba2b18200d09`

```dockerfile
```

-	Layers:
	-	`sha256:cb5405c0c6243c72e4e184f60d6d03110ac49b593595010bc8bec2a0514d03e3`  
		Last Modified: Tue, 16 Jun 2026 01:23:28 GMT  
		Size: 176.1 KB (176122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32ade174178df9ff9e79526d869457c938ff2c802aec35f4f65682e5027c48e5`  
		Last Modified: Tue, 16 Jun 2026 01:23:27 GMT  
		Size: 25.2 KB (25223 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:d10fad1436c6af1537680465cf56e155f1b2beb78dd8d9e7e2e8efe292d3c5a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (100976715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a995728410e7bd131bff830db87e84366ac1479ca2def5f3c73be18064df73a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 01:17:56 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Jun 2026 01:19:56 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jun 2026 01:19:56 GMT
ENV GOPATH=/go
# Tue, 16 Jun 2026 01:19:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 01:19:56 GMT
COPY /target/ / # buildkit
# Tue, 16 Jun 2026 01:19:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jun 2026 01:19:59 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79453f87a61754e860a8bd0c97064515f024688c8847f58cdac4f3ce935a788`  
		Last Modified: Tue, 16 Jun 2026 01:20:14 GMT  
		Size: 247.5 KB (247495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecdc6f594300f89ac123e28e6396b82aeb7db11414dbbf3d120d335b23be9022`  
		Last Modified: Mon, 15 Jun 2026 23:26:34 GMT  
		Size: 96.5 MB (96546025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9508facec9aae50bf95e9522b03a19d9b0e9480482b8441330e8ba2322b332f`  
		Last Modified: Tue, 16 Jun 2026 01:20:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:64cc527e5fd578ee40c1e920a56116eed808cf5b63a0ad3c9c28d768b08cb644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.4 KB (201413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e117959a46fce3598930a4640db855e9d5e0d0d88d38d4f899b772d8becb2afe`

```dockerfile
```

-	Layers:
	-	`sha256:29b513b0b5f4c8e5eb1c86ebb6f0659900ed712b130d5b09b951f488c7a4bb4d`  
		Last Modified: Tue, 16 Jun 2026 01:20:14 GMT  
		Size: 176.2 KB (176158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f31022596ab3a3eac9734a2552ba6d3df2d07077ae796a736440231e2526c0d5`  
		Last Modified: Tue, 16 Jun 2026 01:20:14 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; 386

```console
$ docker pull golang@sha256:b3b48ee78bf90ab3b8124aba028eb31554af3102321498c7cd3c23f0cd408631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.8 MB (103791046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c97e4199375b5cb7c48bd12d7b99efefea78baa752b1fd866b35a5cec72c2f9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:19 GMT
ADD alpine-minirootfs-3.24.1-x86.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 01:14:08 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Jun 2026 01:16:55 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jun 2026 01:16:55 GMT
ENV GOPATH=/go
# Tue, 16 Jun 2026 01:16:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 01:16:55 GMT
COPY /target/ / # buildkit
# Tue, 16 Jun 2026 01:16:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jun 2026 01:16:58 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f86df9d778509895efbf9363d8fcb0cbe0b772de536c7218e4c4c947f0be879f`  
		Last Modified: Sun, 14 Jun 2026 06:45:46 GMT  
		Size: 3.7 MB (3670141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2699df00b13040716eb5d7e3602e870a00a8ff4498f00e7e1d4c3eb84c262771`  
		Last Modified: Tue, 16 Jun 2026 01:17:13 GMT  
		Size: 245.6 KB (245606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1792fe3654cd71494db1238d388e796cd8a11c55f4bdc3626b4c71f43b9583c8`  
		Last Modified: Mon, 15 Jun 2026 23:24:36 GMT  
		Size: 99.9 MB (99875141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1d830c3ac0ca56842858ca22c344fd13c0004aaaf32c8e23fe45d9aa92ab9e`  
		Last Modified: Tue, 16 Jun 2026 01:17:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:fd9e91283834affae5c09dca99346c057474fca0910c8f286a9bc523b373e816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.8 KB (201762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec33494a913a0a4fd9136bbd5ea0c48be45ea75458125457e1c4948c84f2ec0`

```dockerfile
```

-	Layers:
	-	`sha256:f95a2ebf88c56d586564a6d10c89ba51b244249cee580fd57a91021b38bafd7f`  
		Last Modified: Tue, 16 Jun 2026 01:17:13 GMT  
		Size: 176.7 KB (176711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1746b1e0664df604090b2bb7c0d57dbcad31a9bc8ec94db730e5c38af1ab3a7`  
		Last Modified: Tue, 16 Jun 2026 01:17:13 GMT  
		Size: 25.1 KB (25051 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:06440c6fd8270de267d82e9d52f96c7cbae3f48258e74989a8a0f9b1ae036698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.6 MB (102560956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:448f56b8f4edbe2bbba67c7e1efdf7bb05d6ae1b533add89af5c36d890d17639`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:15 GMT
ADD alpine-minirootfs-3.24.1-ppc64le.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:15 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:43:42 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 15 Jun 2026 23:35:08 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Jun 2026 23:35:08 GMT
ENV GOPATH=/go
# Mon, 15 Jun 2026 23:35:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:35:08 GMT
COPY /target/ / # buildkit
# Tue, 16 Jun 2026 01:38:09 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jun 2026 01:38:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3ebcdcd395ccee658b9200e4b27d7699e5d6ed9f6c1858dea12781aac519ff59`  
		Last Modified: Sun, 14 Jun 2026 06:46:36 GMT  
		Size: 3.8 MB (3813400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69e5cd9291f73cdfb8a0cc68e49e0664e71ce2e2dca0d970b3b935c603149a9`  
		Last Modified: Tue, 16 Jun 2026 00:44:13 GMT  
		Size: 247.9 KB (247921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89039b34d27b51562a15e0375b32ce61f3263152969c65f76567c3ed39aa8a9`  
		Last Modified: Mon, 15 Jun 2026 23:36:20 GMT  
		Size: 98.5 MB (98499477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2798dd2cd7035abf9d18fa227ad354761b39400173e9ed6c00698f7151d748bb`  
		Last Modified: Tue, 16 Jun 2026 01:38:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:ef42d2e922444dfbad22c05dd18dd316a4d8a68441ff99f248a6e70cd61ff4c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 KB (201302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfbbdb6fc2cbf3aac27a7cdce2b6061ea8b47785bf6c59c84d6e969b2b931c3c`

```dockerfile
```

-	Layers:
	-	`sha256:0589b9a6be3d23eca2f883a5d6bb2e5e13306e224818fdb884970a131c2fb7e0`  
		Last Modified: Tue, 16 Jun 2026 01:38:31 GMT  
		Size: 176.2 KB (176151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:068a1762f8bb235d89e3b295d4b8b8a5507a47cdfd9e5bdcfb973458fcf03750`  
		Last Modified: Tue, 16 Jun 2026 01:38:31 GMT  
		Size: 25.2 KB (25151 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:a64ee83b8f393ba1cfc97eb06c4c5af42b261d3496a69032b85ae94bb888ea7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.2 MB (103229778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15262204017f8268f3fee39dc8f8342910a0ee1cbe90d59cea506d1ca1308b2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 10 Jun 2026 00:23:10 GMT
ADD alpine-minirootfs-3.24.0-riscv64.tar.gz / # buildkit
# Wed, 10 Jun 2026 00:23:10 GMT
CMD ["/bin/sh"]
# Thu, 11 Jun 2026 13:50:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 09 Jun 2026 06:45:18 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jun 2026 06:45:18 GMT
ENV GOPATH=/go
# Tue, 09 Jun 2026 06:45:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 06:45:18 GMT
COPY /target/ / # buildkit
# Sat, 13 Jun 2026 05:41:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sat, 13 Jun 2026 05:41:30 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3d2f730dbeff3c2e957669de5d586604e82939f67ebfd9142872c9ff56603e07`  
		Last Modified: Wed, 10 Jun 2026 00:23:34 GMT  
		Size: 3.6 MB (3591852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e492241adfd0ab06b09ecf82c4496bab422cdafcbfa20aafd63064aea484beaf`  
		Last Modified: Thu, 11 Jun 2026 13:52:46 GMT  
		Size: 290.6 KB (290582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5a55eb95001de7bce5a945456836deb24c4f6ef91e17b9ea69478ba20a16a6`  
		Last Modified: Tue, 09 Jun 2026 06:52:30 GMT  
		Size: 99.3 MB (99347186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a174d2ad1f3c3dfc08aad80231541e16dea278d47fc8dc1f1a56ac59e2c9283e`  
		Last Modified: Sat, 13 Jun 2026 05:42:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:a978e81d101051c4f7f6f83100113b462394cfc44fd24b4a1172487caa5ef885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 KB (218192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766776b863fe00d200f7c82b0e7587b851c3afa3c72b6d17fb09c6b4ad477e84`

```dockerfile
```

-	Layers:
	-	`sha256:f1c58e51d9f88e40e08e21c14f6bd8c572d820a953533bf79aa5263a5ab8d566`  
		Last Modified: Sat, 13 Jun 2026 05:42:49 GMT  
		Size: 193.0 KB (193039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c6ca2662460f0b2acaf15d90050b5b8ed9d4522d94b769514e3f917a329bb9e`  
		Last Modified: Sat, 13 Jun 2026 05:42:49 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; s390x

```console
$ docker pull golang@sha256:6a8e0a1bfe7109a77005ced58f6190f9275f40b39ee98ed226e4133328866c26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104509377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:960b490fb76508798c8ab5138c13bf966033aa835a1764e6f76aabfd60cc7b98`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:21 GMT
ADD alpine-minirootfs-3.24.1-s390x.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:21 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 01:42:23 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 15 Jun 2026 23:24:06 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Jun 2026 23:24:06 GMT
ENV GOPATH=/go
# Mon, 15 Jun 2026 23:24:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:24:06 GMT
COPY /target/ / # buildkit
# Tue, 16 Jun 2026 01:45:33 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jun 2026 01:45:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:da43be6afaaa3ec1b607461ce64380942a6d76c3d52cda4337b0770d9a96fa89`  
		Last Modified: Sun, 14 Jun 2026 06:47:25 GMT  
		Size: 3.7 MB (3709320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966d2950ecf1fa8cffdbcbcd33f5886abd96dc20b5a21072825c5b3f58cd613c`  
		Last Modified: Tue, 16 Jun 2026 01:45:48 GMT  
		Size: 246.1 KB (246142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0ac3a6fe312cf44641985605a72c55cfb44387624bfcf4ae9738ab565d3ad9`  
		Last Modified: Mon, 15 Jun 2026 23:24:39 GMT  
		Size: 100.6 MB (100553757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58483cfcc0ae82199e6ba39ee7131398f69015166753c8ca12a7bf53908c0200`  
		Last Modified: Tue, 16 Jun 2026 01:45:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:e082ccbbb707c04281107af47d6c7f5bd94fdcde86267f548e814fe93c0f49b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.9 KB (201948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:782ea85fa8b533fcd026959d4a617ac25a435d945312c70ed7a530be1b71d539`

```dockerfile
```

-	Layers:
	-	`sha256:7848f92465413f38a21153e18a05bfd74f1636c6dfa8b980378eea1d323f0e2e`  
		Last Modified: Tue, 16 Jun 2026 01:45:50 GMT  
		Size: 176.8 KB (176849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d9f8629ff8df05e54d515171546eff74e189ae976bc014aa0ca610ae635181`  
		Last Modified: Tue, 16 Jun 2026 01:45:48 GMT  
		Size: 25.1 KB (25099 bytes)  
		MIME: application/vnd.in-toto+json
