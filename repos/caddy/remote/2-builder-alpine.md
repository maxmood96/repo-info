## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:dcf4a528f3f467a5481bbead982228e3e8d38672303fda21a5921857d5200cc1
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `caddy:2-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:47d135ca8690631e46a004ba0825e16286b7052b5ee6396c525ee0821e756678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80715088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4866766977228bff1a8262b6817cd701df695b1091fb68550995c96210eb44cc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOLANG_VERSION=1.22.8
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOPATH=/go
# Tue, 04 Jun 2024 22:12:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 22:12:59 GMT
COPY /target/ / # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
WORKDIR /go
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XCADDY_VERSION=v0.4.2
# Tue, 04 Jun 2024 22:12:59 GMT
ENV CADDY_VERSION=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XCADDY_SETCAP=1
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		riscv64) binArch='riscv64'; checksum='afaf940189942adfe0518d06b42f2624f387a02d88ce9ec5f8cc5a99347e032e2dcae3e3cd5856ac1a6ce107a7654e62b04f635f1dd891ca192b23758946b45b' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e46eeee1980bded4200996c95bcb0d9e56d65535b34e8d17fba7c2475efd48`  
		Last Modified: Tue, 01 Oct 2024 22:18:56 GMT  
		Size: 290.9 KB (290883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfbe2417dd5c75643a7cf33beb58879916ff994a5f80cbdb67cdc3c3528204b`  
		Last Modified: Tue, 01 Oct 2024 22:18:57 GMT  
		Size: 69.4 MB (69361061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c3b7d905597ae4515eb10ff62f331977870d9c31eb499508cf978b5d2279bf`  
		Last Modified: Tue, 01 Oct 2024 22:18:55 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45776380f5e3189092dbad3be11f05d11a87c13eb493758a1f1d0fec494e1cd0`  
		Last Modified: Tue, 01 Oct 2024 22:57:50 GMT  
		Size: 5.9 MB (5938073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed81dd42bd1914780115087be1004397927a3989e557db91e8b83c9db8ed06b`  
		Last Modified: Tue, 01 Oct 2024 22:57:50 GMT  
		Size: 1.5 MB (1500674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697c7883a9489552b848f267828edb28e588c8c3359394454e9038119686988f`  
		Last Modified: Tue, 01 Oct 2024 22:57:50 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:eb50158c07763262fcf495b772edf6f842d0067a8d4db45433b3a8c4527e3bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.0 KB (307987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c36e61cc558c92128c68157a059af3a3b67a794f2027fe2dbbb55c2c6fdd93`

```dockerfile
```

-	Layers:
	-	`sha256:76d6d0af282b2504fa9359488f8831b8a1080163a2db9dcdc208aac4e0344a36`  
		Last Modified: Tue, 01 Oct 2024 22:57:50 GMT  
		Size: 287.9 KB (287913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78774cb4678ee34b9b01a883e71a2e546c489135db2139709936d514f2f4ce7b`  
		Last Modified: Tue, 01 Oct 2024 22:57:50 GMT  
		Size: 20.1 KB (20074 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:31ef46e2b663a7805b2f1a39d12e56c4e58bd28a8dabde4cafbd89d8218556af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78699833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:922bcab905e71eb324ce556e7b68a109c31d490ec1e11e14a2d7f347d08cb37b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOLANG_VERSION=1.22.8
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOPATH=/go
# Tue, 04 Jun 2024 22:12:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 22:12:59 GMT
COPY /target/ / # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
WORKDIR /go
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XCADDY_VERSION=v0.4.2
# Tue, 04 Jun 2024 22:12:59 GMT
ENV CADDY_VERSION=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XCADDY_SETCAP=1
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		riscv64) binArch='riscv64'; checksum='afaf940189942adfe0518d06b42f2624f387a02d88ce9ec5f8cc5a99347e032e2dcae3e3cd5856ac1a6ce107a7654e62b04f635f1dd891ca192b23758946b45b' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b15e82573debca2fd0fd40f07ac032fefe7f9180bd45f4f9cf2c2afde7d486`  
		Last Modified: Sat, 07 Sep 2024 02:30:42 GMT  
		Size: 291.8 KB (291766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061f352dd98f94139dcd80f1ed55842efcd6604bb60fea01003a1fe4ce956ad9`  
		Last Modified: Tue, 01 Oct 2024 22:21:17 GMT  
		Size: 67.7 MB (67735284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022878e6105bfc93899879cb524a4d55ae5506ab7060f6fdf42df91b8138c76e`  
		Last Modified: Tue, 01 Oct 2024 22:21:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b2c82056f92d0a79a2a6693de49e63962cb74d652d6b5258096408f0c2c08d`  
		Last Modified: Tue, 01 Oct 2024 23:50:01 GMT  
		Size: 5.9 MB (5881867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:befe2b11961e8d73387c688fd737eaa597a034357dd2cfe4b60d04320aeeb1cd`  
		Last Modified: Tue, 01 Oct 2024 23:50:01 GMT  
		Size: 1.4 MB (1423815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c57fce1a7d81cf73fe0a23a412695c4e7016a51458d2e52978958f35d6369a`  
		Last Modified: Tue, 01 Oct 2024 23:50:01 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:050fc49affb0d5b94fffdd8e4f2b282b7412e44b96d6e8f320199e59158f7a12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ca1dbf5c927ddc028d7fe3ec43b361ee1dd70caca11eaa324287a0d0575190`

```dockerfile
```

-	Layers:
	-	`sha256:cba3bdac231274a61e80841cfbaff85f06797b40500246667d4a30a2d077095d`  
		Last Modified: Tue, 01 Oct 2024 23:50:01 GMT  
		Size: 20.0 KB (20006 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:cce9169a916af75f8ddba4610f13e60f3ef9f9a3651045a07e6e6a50188023f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77895444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df2ab0c570a51f59147845bb2e4463bdfc3908e461a2867d626cf244d051928`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOLANG_VERSION=1.22.7
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOPATH=/go
# Tue, 04 Jun 2024 22:12:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 22:12:59 GMT
COPY /target/ / # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
WORKDIR /go
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XCADDY_VERSION=v0.4.2
# Tue, 04 Jun 2024 22:12:59 GMT
ENV CADDY_VERSION=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XCADDY_SETCAP=1
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		riscv64) binArch='riscv64'; checksum='afaf940189942adfe0518d06b42f2624f387a02d88ce9ec5f8cc5a99347e032e2dcae3e3cd5856ac1a6ce107a7654e62b04f635f1dd891ca192b23758946b45b' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354df8adec1f26ac2f376cb666910440b4b25a704fec8a3d318f7aff11e80108`  
		Last Modified: Sat, 07 Sep 2024 02:43:40 GMT  
		Size: 290.9 KB (290948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8f557c88424cd7ad839406c3112931cff562d2338fa996a197027ebd6168e0`  
		Last Modified: Fri, 06 Sep 2024 05:28:17 GMT  
		Size: 67.7 MB (67732880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a534f2f3694fe8f49998b8de7c4b139ae017cd210ffd2f421434166e03ab2aff`  
		Last Modified: Sat, 07 Sep 2024 02:45:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d08c88e07dc10f9bc7e6f6ce8e370cbdcffcd5c8d8824b88f5cd8923193fa4a`  
		Last Modified: Sat, 07 Sep 2024 13:51:44 GMT  
		Size: 5.4 MB (5354758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e964d49a4714bb359180b564d910bad5b34cbbf0dc6bc33f2b5c926cfd1bcaa`  
		Last Modified: Sat, 07 Sep 2024 13:51:44 GMT  
		Size: 1.4 MB (1420762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a6e002424f5f889aecba3af0f9be334f33304722367c86d332edca24097091`  
		Last Modified: Sat, 07 Sep 2024 13:51:44 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:e49eec711d6be130e6ed36f6ef7d0e8ac0ac357317ca500e8d8298ac25d2a246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.7 KB (309685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b5d1c2bdebfd939018246b676bbf31def5240fc46176b3999e5d319f759a1b6`

```dockerfile
```

-	Layers:
	-	`sha256:b0ad7327557e70ae5625603adf9d6a597a59ce6e57b46425b1ed4cf9a14e55e5`  
		Last Modified: Sat, 07 Sep 2024 13:51:44 GMT  
		Size: 289.5 KB (289465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9257b811a0d5eae47201498f22e9afbdc95c88f1acfc098b1439740b9d1198e`  
		Last Modified: Sat, 07 Sep 2024 13:51:44 GMT  
		Size: 20.2 KB (20220 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:06c64bb0e97f77a2bd5961aa36f9a9597633fd14763757a51d34336b4ddbd524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78107015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:368fcb24cfa4005f7356e99a5a1492777be9172f04b1632efaa19fc07c6f321f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOLANG_VERSION=1.22.7
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOPATH=/go
# Tue, 04 Jun 2024 22:12:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 22:12:59 GMT
COPY /target/ / # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
WORKDIR /go
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XCADDY_VERSION=v0.4.2
# Tue, 04 Jun 2024 22:12:59 GMT
ENV CADDY_VERSION=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XCADDY_SETCAP=1
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		riscv64) binArch='riscv64'; checksum='afaf940189942adfe0518d06b42f2624f387a02d88ce9ec5f8cc5a99347e032e2dcae3e3cd5856ac1a6ce107a7654e62b04f635f1dd891ca192b23758946b45b' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cac1a4b065c9c855fffe18402bb1a7f6f7e3d3c997a5d6efece488ea46d240e`  
		Last Modified: Sat, 07 Sep 2024 05:15:25 GMT  
		Size: 293.5 KB (293502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e22f72b836bf3633103ff91c50db9b36ba220b58376e9f5fc91490e0e05fd33`  
		Last Modified: Thu, 05 Sep 2024 22:11:49 GMT  
		Size: 66.3 MB (66288032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86670d87c08ae0ecf74a8789044a6fb817373754145afc6e8824becd2e7dbedd`  
		Last Modified: Sat, 07 Sep 2024 05:16:31 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ce5145d56ef4eb949d66069b50dbff42e1539a4cf7482fd2af6e0393fc4cff`  
		Last Modified: Sat, 07 Sep 2024 13:34:58 GMT  
		Size: 6.0 MB (6040081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ccbbb9ef5872d1f8204cb03cbe3b8ec55f8ab3a2a6fd3bb57c5228dc2fb0114`  
		Last Modified: Sat, 07 Sep 2024 13:34:58 GMT  
		Size: 1.4 MB (1397166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb7ca29d7bf7d906c2f073a6b0defbe13013dcc24753774df220719cbef2825`  
		Last Modified: Sat, 07 Sep 2024 13:34:58 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:fbc68ee4a7ac6ced3d99d735d6f6809d0f40c12c678c99a425d7a418e0d5508b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.2 KB (307203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbe0d6241dace0f22d3ab2f97e974edb4627264ba7a67b04b3f5f78f4ab2f4de`

```dockerfile
```

-	Layers:
	-	`sha256:5ed3984e0f433e6352deb00ce5067c5cd4b26f552731e484e0bc749b5666a280`  
		Last Modified: Sat, 07 Sep 2024 13:34:58 GMT  
		Size: 286.7 KB (286671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e70b0ec7f7f5405ce74554fa482dcee4f789c96be9004fffb26b546cb0e1404`  
		Last Modified: Sat, 07 Sep 2024 13:34:57 GMT  
		Size: 20.5 KB (20532 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:629e833b7f02867152244c2577f19e56cce8606dc2b43234e4eb3b19ac3ba211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77974263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9babbba5e9f779158b4a9747b73285de8a71d40419819cb62f56b8544522d8f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOLANG_VERSION=1.22.8
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOPATH=/go
# Tue, 04 Jun 2024 22:12:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 22:12:59 GMT
COPY /target/ / # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
WORKDIR /go
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XCADDY_VERSION=v0.4.2
# Tue, 04 Jun 2024 22:12:59 GMT
ENV CADDY_VERSION=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XCADDY_SETCAP=1
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		riscv64) binArch='riscv64'; checksum='afaf940189942adfe0518d06b42f2624f387a02d88ce9ec5f8cc5a99347e032e2dcae3e3cd5856ac1a6ce107a7654e62b04f635f1dd891ca192b23758946b45b' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2777b92ee7dc04466b000faa6509a7d3ab582a06829100a0e5946b4fe3b87b2c`  
		Last Modified: Tue, 01 Oct 2024 22:26:01 GMT  
		Size: 294.0 KB (294025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2914fcf5f04bc6473e8508cb311821143e30e207b2211825bdb016e893440cf`  
		Last Modified: Tue, 01 Oct 2024 22:28:04 GMT  
		Size: 66.5 MB (66456089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69daf7bedd76e0bb8122b2f1deb0df9c7c06a8105ac8229acaa353e231fafae`  
		Last Modified: Tue, 01 Oct 2024 22:28:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5215d44b732f0978fd9e9e33d525ceeb1bf7210f95295f008bd03b2076f7b861`  
		Last Modified: Wed, 02 Oct 2024 01:21:41 GMT  
		Size: 6.3 MB (6261108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dadaffa3b7dda6822ef98b048a0536a20c62560e62cd600e48d38d3ba4ccf89f`  
		Last Modified: Wed, 02 Oct 2024 01:21:41 GMT  
		Size: 1.4 MB (1390030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8cd82f361669925ac6c293f8760dcf9dad8d83a0dbe91e644b9b328ddafc844`  
		Last Modified: Wed, 02 Oct 2024 01:21:40 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:7edc0fff2bd4de902f2591997b2df591c0ae9dee595c723e2e2566cdefc037c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.2 KB (306225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f7f60fc04de78222ec3ed55998ca5a0ff486961874d3ef607c6f9f0b1eafe5`

```dockerfile
```

-	Layers:
	-	`sha256:22f73644dbdadd90ff3bd15401d0e3225c381db91b2cbb8e1dde745546b66108`  
		Last Modified: Wed, 02 Oct 2024 01:21:40 GMT  
		Size: 286.1 KB (286051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15a3836c9ddbe642ccf6520657f5e595f074019fd6b8a27759a1448099fccc11`  
		Last Modified: Wed, 02 Oct 2024 01:21:40 GMT  
		Size: 20.2 KB (20174 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:b476a551d4bac320dae68b9fd58bed87d5ec443105b8758a6ea9e64725a54850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78125274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d21a69378cf9b88405b6e86f1f3b276ed168512c39595e3bf758a5b0ff9ca3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOLANG_VERSION=1.22.8
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOPATH=/go
# Tue, 04 Jun 2024 22:12:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 22:12:59 GMT
COPY /target/ / # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
WORKDIR /go
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XCADDY_VERSION=v0.4.2
# Tue, 04 Jun 2024 22:12:59 GMT
ENV CADDY_VERSION=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XCADDY_SETCAP=1
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		riscv64) binArch='riscv64'; checksum='afaf940189942adfe0518d06b42f2624f387a02d88ce9ec5f8cc5a99347e032e2dcae3e3cd5856ac1a6ce107a7654e62b04f635f1dd891ca192b23758946b45b' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d1647e2ae8eb941891fcb716820e5bec12b348afc0d29dbe6ad642a22cf24a`  
		Last Modified: Sat, 07 Sep 2024 18:50:29 GMT  
		Size: 291.7 KB (291675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420fd5884781581c953c4b259fb63ef5d96a61c9d361ff1ae9d2cdab761e9598`  
		Last Modified: Tue, 01 Oct 2024 22:40:30 GMT  
		Size: 66.9 MB (66903654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9ed9a69b0c542bfbc2d246512277e5029344100f0edfe10109287c8c4cb389`  
		Last Modified: Tue, 01 Oct 2024 22:40:20 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58755131a815ac11ac94a07aec8296b9c96f30dd65c61d7d933f1f2bb2a5b69`  
		Last Modified: Tue, 01 Oct 2024 23:10:13 GMT  
		Size: 6.2 MB (6153610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b264e50f0cdcfd29070c7efe6821ee638383b8c7a074aaa51bbe4d9d7af6bf0`  
		Last Modified: Tue, 01 Oct 2024 23:10:12 GMT  
		Size: 1.4 MB (1404294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba9478655a7b2e8d7d4f6b30545551cc0bcba75bdefa80bf95a22f2084ab78a`  
		Last Modified: Tue, 01 Oct 2024 23:10:11 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:409e6458d11391f84fbc3742d2382d4f351617febf190245e0452d443c029120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.2 KB (306221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28274757c823326cc691d254e9253d2fce2db5213828804c45b59ca43cb8d05a`

```dockerfile
```

-	Layers:
	-	`sha256:e498fda512e0fa18301a30a2a10333dd03962e9fa480bdc6fc4df51945ad6126`  
		Last Modified: Tue, 01 Oct 2024 23:10:11 GMT  
		Size: 286.0 KB (286047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04ba8ba3e852aa876d791768fc4c3e3c43280d611a90ff5862584177328119bd`  
		Last Modified: Tue, 01 Oct 2024 23:10:11 GMT  
		Size: 20.2 KB (20174 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:8bb41beaf13e61e2b7ca2cad38011ec967133053482ca4b25b0e4a705dc5b29d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79827721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b4257e8236ea326bf6582d18a1075b0d3c763905f70369d53a4b03794727759`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOLANG_VERSION=1.22.8
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOPATH=/go
# Tue, 04 Jun 2024 22:12:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 22:12:59 GMT
COPY /target/ / # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
WORKDIR /go
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XCADDY_VERSION=v0.4.2
# Tue, 04 Jun 2024 22:12:59 GMT
ENV CADDY_VERSION=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XCADDY_SETCAP=1
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		riscv64) binArch='riscv64'; checksum='afaf940189942adfe0518d06b42f2624f387a02d88ce9ec5f8cc5a99347e032e2dcae3e3cd5856ac1a6ce107a7654e62b04f635f1dd891ca192b23758946b45b' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c6a0ddb32c239716405fcb244342a8d9c9657fd7f86e86d8b5d11ec45f0543`  
		Last Modified: Tue, 01 Oct 2024 22:22:42 GMT  
		Size: 291.9 KB (291893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633cee5ad69619a965adbb356b33056233e255849ab3de138bcc483803c988f6`  
		Last Modified: Tue, 01 Oct 2024 22:24:55 GMT  
		Size: 68.4 MB (68420831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d405b4ebe9ac59b9eafbba27feb020a1787cce12a2833b547fe2979e6503d1b`  
		Last Modified: Tue, 01 Oct 2024 22:25:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254b4153e6d1a85ea5f7160d338a4a8fba5a493da01b9c10289dc7aadd363f4b`  
		Last Modified: Wed, 02 Oct 2024 01:41:39 GMT  
		Size: 6.2 MB (6201022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d87b3d6de144fe63f5f92b25516f1e66adc2c865ffc6f6deba97f2f3b5aed1`  
		Last Modified: Wed, 02 Oct 2024 01:41:39 GMT  
		Size: 1.5 MB (1451785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ea2165b9a11aca569fa0a7e40f051b27fb97f39a81e2f3881bbb7393cf088d`  
		Last Modified: Wed, 02 Oct 2024 01:41:38 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:358ef6dbb51ecd06147193bbdc63c7cfa965b82c6b5b260187f116a56d205e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.1 KB (306063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7509356b912c5608fae91489fd360809846c92f66da1c4043e235ec7cb77fa5f`

```dockerfile
```

-	Layers:
	-	`sha256:4af996c4680c735ee08674dec50356bfb86606a9eae27fd0a98d35a39b8f6b3f`  
		Last Modified: Wed, 02 Oct 2024 01:41:38 GMT  
		Size: 286.0 KB (285959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4ca54c4be6f42f0748974c9e05a5789b3cfcb2add163d11fa7c71b6fe629cd0`  
		Last Modified: Wed, 02 Oct 2024 01:41:38 GMT  
		Size: 20.1 KB (20104 bytes)  
		MIME: application/vnd.in-toto+json
