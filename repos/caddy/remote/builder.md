## `caddy:builder`

```console
$ docker pull caddy@sha256:8778619a8bfd796c5bafa16a1273e092612c57b34e25cb62d12ea6636f1ae252
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `caddy:builder` - linux; amd64

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

### `caddy:builder` - unknown; unknown

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

### `caddy:builder` - linux; arm variant v6

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

### `caddy:builder` - unknown; unknown

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

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:ec90f02a1b74820ec988510ac152855fa807a19a64d86e683477bfb9e07b24e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77910335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e662859717895bdba3e7d49aff9ff5ba2e53dfc3a0fdd6d82622a2508e99301`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
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
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354df8adec1f26ac2f376cb666910440b4b25a704fec8a3d318f7aff11e80108`  
		Last Modified: Sat, 07 Sep 2024 02:43:40 GMT  
		Size: 290.9 KB (290948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b4f9ce39f7d429108bcb97e8c76dfe3aa89153860baa24a03d32de7ae05005`  
		Last Modified: Tue, 01 Oct 2024 22:26:31 GMT  
		Size: 67.7 MB (67735116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf420245d925539c66d6160262a1fb89fe2c54b7c65d67c03b5836c5ed529b68`  
		Last Modified: Tue, 01 Oct 2024 22:27:56 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1565bba492483471cc7e89d6ad15bf78ed75eaa14c02602bcc3d66b4a84e028f`  
		Last Modified: Wed, 02 Oct 2024 03:58:45 GMT  
		Size: 5.4 MB (5367416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb6ef444f9fabd0d177b8caec40666f98d96dc3229de0c45caf61694a5f0971`  
		Last Modified: Wed, 02 Oct 2024 03:58:45 GMT  
		Size: 1.4 MB (1420762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0bf0500036eba888f0a7c13a4cce1b1bac689991c89d3d14c7d37ef781c1266`  
		Last Modified: Wed, 02 Oct 2024 03:58:45 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:31c5054c89d945d30a6f18def52156cbb4217e65decf365fe759a37db0b85118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.0 KB (311036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa4b60bb0e88e9a811a65d096554284e828fae65810f0a2eb7d982eb8eb59bfd`

```dockerfile
```

-	Layers:
	-	`sha256:c79bf64856c90045121a2382f3fb151ee4deb7aa0457b44c86b39c7f3c9c01ec`  
		Last Modified: Wed, 02 Oct 2024 03:58:45 GMT  
		Size: 290.8 KB (290811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53dfd26e78840b1ea61f8766ae943191c4ba31eb18535815629a2f1cf5f856e5`  
		Last Modified: Wed, 02 Oct 2024 03:58:45 GMT  
		Size: 20.2 KB (20225 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:e0f0bddac97558aef01592b12f3dd1010a33e527aa4abbedb2d8cf3aa0f984ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78126282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:782dcd272ecc9b582317558f16962747c77e6e250a3c0d2f51ca466a58164b9e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b35a11ae5eab5f9885f480b702f14893ab21d2d29f58cd678d35d2fde98e27`  
		Last Modified: Tue, 01 Oct 2024 22:23:44 GMT  
		Size: 293.5 KB (293518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c762012eccac2a235149075018bdac991ee64160ef613d720fb8e7c4153acd55`  
		Last Modified: Tue, 01 Oct 2024 22:26:07 GMT  
		Size: 66.3 MB (66290538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202bfe40db516da49fcc36cf98fd5d107c2132a268131661942b5eb40d50dabc`  
		Last Modified: Tue, 01 Oct 2024 22:27:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c3a96e0cd8dcd922698dc479f9470a2d07a11b8afd7ffad80c6eb438781baa`  
		Last Modified: Wed, 02 Oct 2024 04:53:25 GMT  
		Size: 6.1 MB (6056821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c382cccca473e2e6e94bf6425129d2a5ea7fbbdffa4f02bfedba007fd8528ee4`  
		Last Modified: Wed, 02 Oct 2024 04:53:25 GMT  
		Size: 1.4 MB (1397169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992564cfb2a45a220a05b02eeff1deb9140abbb0a3d9682f8087b73ece8871f2`  
		Last Modified: Wed, 02 Oct 2024 04:53:24 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:8915c6a89b4fd3b5c28f7c1b902e2ccdbac5f65560afe11a8a68347c06148a13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.3 KB (308288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e548670f87471378ef3ed4e4f91a48aff6d5bcb4c136d2bb716dd77625cc0f`

```dockerfile
```

-	Layers:
	-	`sha256:d1182931a028eeb67b8febae22b3d32f975f9cb9250a03297a22fb543c65e1bc`  
		Last Modified: Wed, 02 Oct 2024 04:53:24 GMT  
		Size: 288.0 KB (288017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4860e5ddc7cc15886f0fbe130c91a5a33a1f2ed9ef1a2cf5bbfab30463c7f57`  
		Last Modified: Wed, 02 Oct 2024 04:53:24 GMT  
		Size: 20.3 KB (20271 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; ppc64le

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

### `caddy:builder` - unknown; unknown

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

### `caddy:builder` - linux; riscv64

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

### `caddy:builder` - unknown; unknown

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

### `caddy:builder` - linux; s390x

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

### `caddy:builder` - unknown; unknown

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

### `caddy:builder` - windows version 10.0.20348.2762; amd64

```console
$ docker pull caddy@sha256:6ac83b1c26ac7aaf35b0837eaeb438f53947f5493e08a05df524aafff76edcfa
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1898983706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc08ee02fe68def75c76b8da74205c43d2528ef4700fb87f0a77b2b7fabc751`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Wed, 09 Oct 2024 23:07:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 23:07:19 GMT
ENV GIT_VERSION=2.23.0
# Wed, 09 Oct 2024 23:07:20 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 09 Oct 2024 23:07:21 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 09 Oct 2024 23:07:22 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 09 Oct 2024 23:07:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Oct 2024 23:07:52 GMT
ENV GOPATH=C:\go
# Wed, 09 Oct 2024 23:07:57 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Oct 2024 23:07:58 GMT
ENV GOLANG_VERSION=1.22.8
# Wed, 09 Oct 2024 23:09:54 GMT
RUN $url = 'https://dl.google.com/go/go1.22.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9eca39a677c6d055ed947087c63e430b2c6d5dd0dd84636cb171fa2717451ee1'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Oct 2024 23:09:55 GMT
WORKDIR C:\go
# Thu, 10 Oct 2024 00:02:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Oct 2024 00:02:35 GMT
ENV XCADDY_VERSION=v0.4.2
# Thu, 10 Oct 2024 00:02:35 GMT
ENV CADDY_VERSION=v2.8.4
# Thu, 10 Oct 2024 00:02:36 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Oct 2024 00:02:50 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 10 Oct 2024 00:02:51 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84c6a3bb7513442bf3ea36a61c841c9d51c9b0eda57fa5102de561f0168b9efe`  
		Last Modified: Wed, 09 Oct 2024 23:10:00 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a89b3526bff882cf74613bb96be2cf0a70c32c8f9ca23071d107e88bcc8fae4`  
		Last Modified: Wed, 09 Oct 2024 23:10:00 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4ee90109c2fc409f0fe8703f363226e2ccd94f583f25d692d1298fd044e22d`  
		Last Modified: Wed, 09 Oct 2024 23:09:59 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c4a8072b43719b2ba31e746cd37606f6f71841fba288e4398249e30b9cb549`  
		Last Modified: Wed, 09 Oct 2024 23:09:59 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238a1a479f8a3cd894683d4c87de3b9c746a92035eacd7df9fcc2859b09b0e36`  
		Last Modified: Wed, 09 Oct 2024 23:09:59 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f688d2c11cef151a74584464154fc80277da1051b962c73d2371aea3aaac84ad`  
		Last Modified: Wed, 09 Oct 2024 23:10:02 GMT  
		Size: 25.6 MB (25568209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b740bc876b54f50f96920bc5988698c0af48bf787f327711329249e51189bf`  
		Last Modified: Wed, 09 Oct 2024 23:09:58 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb8b11c005e57c2d0f7297469fa08edf19e6e2e67d9cc4213681a27758d32eb3`  
		Last Modified: Wed, 09 Oct 2024 23:09:58 GMT  
		Size: 337.7 KB (337688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5f2d857ee89aca09581ccfff2c3bc1ae53b419310f40bad9dd097e34448a36`  
		Last Modified: Wed, 09 Oct 2024 23:09:58 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd91c040da99d28ae85178f2763876b1d31a211b1cb26770518cd37038e6c621`  
		Last Modified: Wed, 09 Oct 2024 23:10:09 GMT  
		Size: 71.8 MB (71762980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69550b1669145855ed0001c29e3ff1b2386cd5cb890b7ab4b25154e4fe4ab4c5`  
		Last Modified: Wed, 09 Oct 2024 23:09:58 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50675065a62898dc90f4ebe5b2fa6f639c44e1f55c098800a2373fdf75b58b41`  
		Last Modified: Thu, 10 Oct 2024 00:02:54 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87adc048cd0461f8f5bc400783342917c4f5ae97e53fc1a07cfb449db9aaec19`  
		Last Modified: Thu, 10 Oct 2024 00:02:53 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c972986a6c9ba802edc83b141060f1ea9a7b524ae50723a45409d29a299d8722`  
		Last Modified: Thu, 10 Oct 2024 00:02:53 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79a8f3f0eac0236760104ff698e264dd715c3e4f8bd796801e6264383a2c66dc`  
		Last Modified: Thu, 10 Oct 2024 00:02:53 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68813ae6b8ff81157af74bb283b047ef37089db148eb954f218b3d1e9fcb325f`  
		Last Modified: Thu, 10 Oct 2024 00:02:53 GMT  
		Size: 2.0 MB (1956341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6bcfb2d6911d1e0865b9d5f17683ea10c76e94f36c8a332ce010208d9aac30`  
		Last Modified: Thu, 10 Oct 2024 00:02:53 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.17763.6414; amd64

```console
$ docker pull caddy@sha256:e4cefb4071950d5aab1e4d40aff6fa6d637ef02cc00e0dc969bd90fde8377e19
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2001370618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c445072d5ffc307cc66716f69c240d0a9a5bb15fced88a0b343e802f5a945af5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Wed, 09 Oct 2024 23:08:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 23:08:55 GMT
ENV GIT_VERSION=2.23.0
# Wed, 09 Oct 2024 23:08:55 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 09 Oct 2024 23:08:56 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 09 Oct 2024 23:08:57 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 09 Oct 2024 23:09:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Oct 2024 23:09:21 GMT
ENV GOPATH=C:\go
# Wed, 09 Oct 2024 23:09:28 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Oct 2024 23:09:28 GMT
ENV GOLANG_VERSION=1.22.8
# Wed, 09 Oct 2024 23:11:25 GMT
RUN $url = 'https://dl.google.com/go/go1.22.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9eca39a677c6d055ed947087c63e430b2c6d5dd0dd84636cb171fa2717451ee1'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Oct 2024 23:11:27 GMT
WORKDIR C:\go
# Thu, 10 Oct 2024 00:09:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Oct 2024 00:10:02 GMT
ENV XCADDY_VERSION=v0.4.2
# Thu, 10 Oct 2024 00:10:03 GMT
ENV CADDY_VERSION=v2.8.4
# Thu, 10 Oct 2024 00:10:04 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Oct 2024 00:11:27 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 10 Oct 2024 00:11:28 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d98338b2e4dc07085c57a4ef58778d8a6b8e63aa1264a2528cb736d20a41cc`  
		Last Modified: Wed, 09 Oct 2024 23:11:31 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6f4380d133dfd5411c4a9044b299cbec74a42422ce46717616f0006c7f7312`  
		Last Modified: Wed, 09 Oct 2024 23:11:31 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffe9e0487c26c1f87199246cb767893db54453eda086fe5845debdba5ece054`  
		Last Modified: Wed, 09 Oct 2024 23:11:30 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e697b7352baf280e194ecdfecbdc738cc06c682e65ee512996ce8b111cfb5a`  
		Last Modified: Wed, 09 Oct 2024 23:11:30 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ba684e044b9a5a2475f19a6a9e4cc1b7992fa0c0008c8d4e6b0b3de7601082`  
		Last Modified: Wed, 09 Oct 2024 23:11:30 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc73727502cdd380228172ef3387250c05640b768ecfeab771cc23a8c5d18e4`  
		Last Modified: Wed, 09 Oct 2024 23:11:33 GMT  
		Size: 25.6 MB (25550981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca137ecd94e93e649ae5d9fbc116d48c8ec641f4732b6aca66285edc62f790bd`  
		Last Modified: Wed, 09 Oct 2024 23:11:29 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1c0cff9a356a4ffa2a7be6d1c8e516e6b6226f21f1cbe24360241ccd6908eb`  
		Last Modified: Wed, 09 Oct 2024 23:11:29 GMT  
		Size: 312.2 KB (312154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb6fe2ace5be98a6a690a801319bfdae8eb19a64d048fa533b73eb3c5ed5213`  
		Last Modified: Wed, 09 Oct 2024 23:11:29 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c49ba53c1434fab7fe610dff9b4959e9f557783848c91f82eb4b68cd887f1c6d`  
		Last Modified: Wed, 09 Oct 2024 23:11:40 GMT  
		Size: 71.7 MB (71740842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418de26160b3c625ee85df492e4ad85a7121ae66b294dbe320168c94c445fa20`  
		Last Modified: Wed, 09 Oct 2024 23:11:29 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0659da63a02bc1625a353126a45af35f30de7275e866bcd8000e8a1a65662205`  
		Last Modified: Thu, 10 Oct 2024 00:11:31 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53fc69905e94b4666864ac1f26766604ebc9eb14dd00fd9508c8d3b85c14f93e`  
		Last Modified: Thu, 10 Oct 2024 00:11:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a016131396abc33d78429d7acfc59523b973651586ca1fd65105d4002e210c`  
		Last Modified: Thu, 10 Oct 2024 00:11:30 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd64724861ba42517227869eff9536a70f2b0feb4dda02e1d455aaa4f62d38d`  
		Last Modified: Thu, 10 Oct 2024 00:11:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607ac9ad7d1c108972f7292ea89a48a7d4405e2d888f260b810565457202a946`  
		Last Modified: Thu, 10 Oct 2024 00:11:30 GMT  
		Size: 1.9 MB (1924253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca928be5f95e4c10c259cebbb6541327ac51365f4814498a7d4cb4a22be3826f`  
		Last Modified: Thu, 10 Oct 2024 00:11:30 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
