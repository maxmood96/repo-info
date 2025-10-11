## `golang:alpine3.22`

```console
$ docker pull golang@sha256:06cdd34bd531b810650e47762c01e025eb9b1c7eadd191553b91c9f2d549fae8
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

### `golang:alpine3.22` - linux; amd64

```console
$ docker pull golang@sha256:2096b2779e9643ea6c987e729c5cc5225c50014bf9d23518cacd4f00c19fb9c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64242934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f87d2639c296390bc3a14ff1eeab4f205119215f27e8c574af7e3f8e496e5314`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 07 Oct 2025 19:07:03 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 19:07:03 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOLANG_VERSION=1.25.2
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOPATH=/go
# Tue, 07 Oct 2025 19:07:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 19:07:03 GMT
COPY /target/ / # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35fb4624d26424571dfb821ae83d912cb463420dcedd6224f36bb5f96f92542`  
		Last Modified: Wed, 08 Oct 2025 23:03:29 GMT  
		Size: 291.1 KB (291148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2aec7ef170b5f02e240ef6c8aac64fb96a14688ea0750c962c145c141f3830`  
		Last Modified: Tue, 07 Oct 2025 20:47:28 GMT  
		Size: 60.1 MB (60149177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333b49ad6fbf2b99bf7532e840b5bff11ea42e960a0a8851832dbe82fa3d7c00`  
		Last Modified: Wed, 08 Oct 2025 23:03:29 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:f74da305e0fa43d9153a1fd055ba585790837b24a2d7e65e3139a53d9ffad637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.6 KB (221632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c027fd15a070b34780ddd696006b684214ad5134a1f98d35aaf31ded177c9d5c`

```dockerfile
```

-	Layers:
	-	`sha256:dc0742292e8e322bb202306b7c0625021a91460a19ea15a8dc64cf27033ba021`  
		Last Modified: Thu, 09 Oct 2025 00:53:21 GMT  
		Size: 195.6 KB (195562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db92057e4a597a8adb7b0072d07e3f4d5f1e46e1ffc01c8c99ab3d7357862c27`  
		Last Modified: Thu, 09 Oct 2025 00:53:22 GMT  
		Size: 26.1 KB (26070 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.22` - linux; arm variant v6

```console
$ docker pull golang@sha256:7686812d6c81ad5766cfda39780af510c7f8117b6c1468bcea7dc74b441c9db5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62870563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6215f3ccb2c1ee425bdd79d3b096dae2be70dbcec48e546cbff419461723cd23`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 07 Oct 2025 19:07:03 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 19:07:03 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOLANG_VERSION=1.25.2
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOPATH=/go
# Tue, 07 Oct 2025 19:07:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 19:07:03 GMT
COPY /target/ / # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60994a2fa6b267edd2843cd5fc3f2d8c2924451ede829846056191379774525`  
		Last Modified: Wed, 08 Oct 2025 22:10:35 GMT  
		Size: 292.3 KB (292299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a729a3e231583976ae1f9cca817bd27dd00673c51d31bb2652e5b51a3d2ea3d`  
		Last Modified: Tue, 07 Oct 2025 19:34:35 GMT  
		Size: 59.1 MB (59074026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a144a8289ff4ec4a0f9128ce6b7dc6f717724bc579d510f16fa276fe7e0ac938`  
		Last Modified: Wed, 08 Oct 2025 22:10:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:3a7f5ce62d6097049cbe693824f8433de5f847aa4df4e8c53ee88c001f6931bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (25993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e49bae024993e6e1fde9a84abc061fa5d852707f53c8ddab04ad098691755646`

```dockerfile
```

-	Layers:
	-	`sha256:d3c41d7513aa6987a6ad380e576a91c6099677186f2c0d8d8b6f74808129d33e`  
		Last Modified: Wed, 08 Oct 2025 23:22:32 GMT  
		Size: 26.0 KB (25993 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.22` - linux; arm variant v7

```console
$ docker pull golang@sha256:32e3b3df810c5eee9b5a6a1667cbdfbdd0c343da516ed5397a9400c32f80ed57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62587009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8cc51ceae8cbfc4fb9f064b0b68187878e05844cd8f1dac3199357e715fbf30`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 07 Oct 2025 19:07:03 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 19:07:03 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOLANG_VERSION=1.25.2
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOPATH=/go
# Tue, 07 Oct 2025 19:07:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 19:07:03 GMT
COPY /target/ / # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2c26235c37292159dc019803ebd2435f82dd20bd64043f085ba7daa47b28c9`  
		Last Modified: Wed, 08 Oct 2025 22:13:09 GMT  
		Size: 291.2 KB (291213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28977543608eb3d47060855462d9576fb750f3b4671b32d32fcc7f41fe2a4f4`  
		Last Modified: Tue, 07 Oct 2025 19:34:15 GMT  
		Size: 59.1 MB (59074083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac6fb7af5cbe0bd826c2f8c108ebcc4a5d1178c58d9f83207a6d0924695cec3`  
		Last Modified: Wed, 08 Oct 2025 22:13:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:316a2c428fdbdb6fba82f5c6324121ad56dffcc4bfd85c944131a313852b85d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 KB (221824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d1f71165f816fe741da0adbb5eafbc61bd338ae41e34b69088c463ec7d1e024`

```dockerfile
```

-	Layers:
	-	`sha256:425c7ff77eef8e95c9d1169c258f5645bd281132b8c412b4a2caf98f13c6558d`  
		Last Modified: Wed, 08 Oct 2025 23:22:35 GMT  
		Size: 195.6 KB (195616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6dc4a2df79f34c1b1a0b2fd09a9b0bf0a184fba75d445986ad3f6ed38ed8039`  
		Last Modified: Wed, 08 Oct 2025 23:22:36 GMT  
		Size: 26.2 KB (26208 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:b6f64a7a84da0455c16d24e7b12927169bf4613cc144cbb9cdd788fdca70cdb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62080136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e252f9315a5d31d9d1d916f6fbd337deef8dca67a18ce555b87a11ddc867584c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 07 Oct 2025 19:07:03 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 19:07:03 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOLANG_VERSION=1.25.2
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOPATH=/go
# Tue, 07 Oct 2025 19:07:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 19:07:03 GMT
COPY /target/ / # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00abc3ba1385e30f6e4c6e0525cb316aa3afd1e3a6ce37bd5dae6bf03aae2b97`  
		Last Modified: Wed, 08 Oct 2025 21:49:25 GMT  
		Size: 294.1 KB (294091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66626199bcfab248906ccbdd0d977cc77ec2231a37f1710a42892109d86b2544`  
		Last Modified: Tue, 07 Oct 2025 19:34:30 GMT  
		Size: 57.6 MB (57647819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89982c427569fa227db8454803b4026b779be40fa10f2a70f135a6fa03475dc`  
		Last Modified: Wed, 08 Oct 2025 21:49:25 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:e36625bfd556735f0b0aad7bfb39bdf93547ced5ef99bba2cc3ac303dd59903a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 KB (221918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:642f834a936abdac547abec167b50c3b3964eedad60e90b8f725ec2cc977fed1`

```dockerfile
```

-	Layers:
	-	`sha256:aa3ae640fc612d5f47055eb2a588379d5f9ce76e62078e4921f5d648a23814cb`  
		Last Modified: Wed, 08 Oct 2025 23:22:39 GMT  
		Size: 195.7 KB (195666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7e1624e77d9b200ba61a8b10528bd6ea855fef4f1c4d5a5300ffb1d940e43d6`  
		Last Modified: Wed, 08 Oct 2025 23:22:40 GMT  
		Size: 26.3 KB (26252 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:8cc7d93ada966e0b8439888412301ef32870ac7d3aedbeda55c0648be4c934d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62780584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:387fb55a71d00fbb73ce88023725b94a17aa790382a184fe9da4b0bd6ce15bbc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 07 Oct 2025 19:07:03 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 19:07:03 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOLANG_VERSION=1.25.2
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOPATH=/go
# Tue, 07 Oct 2025 19:07:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 19:07:03 GMT
COPY /target/ / # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc90e25328cf4b464421f4ebd7975463a91345cb4ffd12c1128a09723ebcab2d`  
		Last Modified: Wed, 08 Oct 2025 21:41:06 GMT  
		Size: 291.6 KB (291633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1303a4fd3683897bef6c94e29bf9e3651f1c90c65f26cacc89697c837708724c`  
		Last Modified: Tue, 07 Oct 2025 19:34:26 GMT  
		Size: 58.9 MB (58869862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e34624565a982f4c9a6ff6c6362d370ff0ae9183af986c25982ea1f118db246`  
		Last Modified: Wed, 08 Oct 2025 21:41:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:a5aa79b5189200231df0ae22ff83816ca4fa23029db8b274eb46d8651563bd2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.5 KB (221517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9c3451e1b9cedcf7390f0ac7f03c3c4001a04d93f561270f01112e7f4862f8`

```dockerfile
```

-	Layers:
	-	`sha256:e841d84c4ce5ad3fd9891c827388869003bfd41180c2d1830490380d29dd83ea`  
		Last Modified: Wed, 08 Oct 2025 23:22:43 GMT  
		Size: 195.5 KB (195503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1d9f4e42d56bf261244f1e46af07e143859c5582968854821d5dac5993cd648`  
		Last Modified: Wed, 08 Oct 2025 23:22:44 GMT  
		Size: 26.0 KB (26014 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.22` - linux; ppc64le

```console
$ docker pull golang@sha256:20e16ace37e696c45f53da94f2588e75a0ea5584ba77399b10d7bc9193ee1a7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62160771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5c56e31c2da1e471394239c6880ec7d00e27b05128e371fe297df25f1b9854`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 07 Oct 2025 19:07:03 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 19:07:03 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOLANG_VERSION=1.25.2
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOPATH=/go
# Tue, 07 Oct 2025 19:07:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 19:07:03 GMT
COPY /target/ / # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e34403a3833161e7317f5f43c031b3114df383a82ea83c5851edc4d5c8b921a`  
		Last Modified: Thu, 09 Oct 2025 04:12:57 GMT  
		Size: 294.6 KB (294579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbab16c006e3e87a0bd86bfecf5ca21f23b4930a744517459433c08bfbfc59e0`  
		Last Modified: Tue, 07 Oct 2025 19:34:11 GMT  
		Size: 58.1 MB (58133794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4273071d0d29fa1710b0b144feb490014c3531d770a922413a9bd76359d9c503`  
		Last Modified: Thu, 09 Oct 2025 04:13:04 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:466253fc7a67d1eb87d2d817c80f028e9a592ab2f785f982dccf33b978714cb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.8 KB (219825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5093dfd70019b54fb233b4c33f30fe01c38c3c695b0df881f45ffd1c05a4311`

```dockerfile
```

-	Layers:
	-	`sha256:77a952ebbf0556309ac8a401921eec6307bb508820f05d54ece3a0222910e94a`  
		Last Modified: Thu, 09 Oct 2025 05:22:35 GMT  
		Size: 193.7 KB (193683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38b118f3a6c72491431cfe8866a2103d53acf5482573bc11eae35159517f2828`  
		Last Modified: Thu, 09 Oct 2025 05:22:35 GMT  
		Size: 26.1 KB (26142 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:dc7e900df436b6cd6c26d9b92f00cd2e28cea0ab1797d40b71e24861d36b405e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62477118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658a42e3b96c30d2381e34f9e40547bdf6313e6abca34eae4f8ddb545c79a607`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 07 Oct 2025 19:07:03 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 19:07:03 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOLANG_VERSION=1.25.2
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOPATH=/go
# Tue, 07 Oct 2025 19:07:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 19:07:03 GMT
COPY /target/ / # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2055b904ba40ebefe03b802bf4885ac2708bb5c47a4294058815bff9a5ca3b`  
		Last Modified: Fri, 10 Oct 2025 21:04:20 GMT  
		Size: 291.5 KB (291511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16d54fbaaf4f44943b5fd17aacabad20b0db0f29394c2b0f581a3a300b124c2`  
		Last Modified: Tue, 07 Oct 2025 19:40:12 GMT  
		Size: 58.7 MB (58670209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a5560ed74dd02976dd5cab3ab4ed0f7f384b6673248ad4d19859acfdb42a3f`  
		Last Modified: Fri, 10 Oct 2025 21:04:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:a5e65e1ddcae1d86c9b6c99c59885285058978ca335f8479bfaab811ccec69fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.8 KB (219819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba21f1117a7692f94d0a720a7e31141bb627ef62aa0cb102bff90322126ad8cf`

```dockerfile
```

-	Layers:
	-	`sha256:84d67dcb5c76868fc07ffbf6a80395f761017e5a69e2ed3150702385bfce9cc3`  
		Last Modified: Fri, 10 Oct 2025 23:22:36 GMT  
		Size: 193.7 KB (193679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36e9da97aca421b097542ab1613b4189c5e055e4f4c2184cb87116a61ea3b46c`  
		Last Modified: Fri, 10 Oct 2025 23:22:36 GMT  
		Size: 26.1 KB (26140 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.22` - linux; s390x

```console
$ docker pull golang@sha256:05e89d59f64f0160b7409e7d141f3ba00c95055bfc7543373305d6513f45d33e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63420365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7bf69dd404f118e8fe40db049d2810aa9e349ebee8e888794d030f66273fa21`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 07 Oct 2025 19:07:03 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 19:07:03 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOLANG_VERSION=1.25.2
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOPATH=/go
# Tue, 07 Oct 2025 19:07:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 19:07:03 GMT
COPY /target/ / # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2de0d30ada31da192f5016a4897bdd65bd1ab1a8a13dcbc1a8bf1e887eba8f`  
		Last Modified: Thu, 09 Oct 2025 02:39:03 GMT  
		Size: 292.2 KB (292158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6429ba33a49b3f3080422ca98d26430f3e1c1ba8f8f41bc6d8af4cff9843f4da`  
		Last Modified: Tue, 07 Oct 2025 19:36:10 GMT  
		Size: 59.5 MB (59478805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc1af17613180179944931e348017c6e19f85695f4ebedf0ef0a4eeb22ea448`  
		Last Modified: Thu, 09 Oct 2025 02:39:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:80a55ebee7665d5f40a5e033d2e80c5c703aaad8633681fa0debff50f43a5f07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.7 KB (219681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:177b076228099e183197c6bec2fd3a79ad24e3296556eacd859a521b855c2af5`

```dockerfile
```

-	Layers:
	-	`sha256:e8c1dec87efc6da4fc74bf95d9edf67e1c0761d89b407f6a9b5af4f9ada60f84`  
		Last Modified: Thu, 09 Oct 2025 05:22:40 GMT  
		Size: 193.6 KB (193611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1eec0e073ae407f0ca1b23833316761a2de68360a7c7b36b6b6254270195e152`  
		Last Modified: Thu, 09 Oct 2025 05:22:41 GMT  
		Size: 26.1 KB (26070 bytes)  
		MIME: application/vnd.in-toto+json
