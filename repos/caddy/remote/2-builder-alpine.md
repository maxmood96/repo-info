## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:21dc27cb6464a19f4f1dbbe66702601c8d860aff1c9c5552097d4743c077be53
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
$ docker pull caddy@sha256:03e55598a22cf3b71d9d88524511f29dbfbd9c5b6a516d8cd72d2fe97ae771ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80699390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eedc44ddd017bfe015d3fd41321df888765852981c76a86a5e960b1e22abefa`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOLANG_VERSION=1.22.6
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
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efce3567381bf30f7ebfb2c0f4530d8a9270632f35e0a39dff013f1a355ff490`  
		Last Modified: Tue, 06 Aug 2024 22:56:12 GMT  
		Size: 290.9 KB (290881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c08045297c877b698a8fa5aa6b5d3ec88c34ba7415eb1f83746a1f6babd1cf`  
		Last Modified: Tue, 06 Aug 2024 22:56:12 GMT  
		Size: 69.4 MB (69362558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0948f4ee3b360384a2d8fe514078b1c47ef2dc81dc723acdc37de37753d2a0a7`  
		Last Modified: Tue, 06 Aug 2024 22:56:11 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2f913719b2332488263223376a9b5e3387c65cbd1485b9eade97d85e460bef`  
		Last Modified: Tue, 06 Aug 2024 23:57:40 GMT  
		Size: 5.9 MB (5921795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310a0f86e894ceda326dfdf36a4a28dbaaef01295f8bae581855f731a1c3a84f`  
		Last Modified: Tue, 06 Aug 2024 23:57:40 GMT  
		Size: 1.5 MB (1500674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5c2c75d18f33fcb6bad189f02df9b6598755f1347b8b3fd1c4b878a639e5ee`  
		Last Modified: Tue, 06 Aug 2024 23:57:40 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:f9a522c4a3a706a3b751eeab512eefc5aa28f3c28dc149173bef180c76bac057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.6 KB (306636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad4cb2ef8d0ae6dab1abdd910a5ab715d73945ca6bd53b3e352721e90d14374`

```dockerfile
```

-	Layers:
	-	`sha256:540328cd899d425e670a513953310adc33263cc69568e0b73056c0d9e3155e71`  
		Last Modified: Tue, 06 Aug 2024 23:57:40 GMT  
		Size: 286.6 KB (286567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8c98082f82f2afd7e90b26a05e8bd96d8ef1dd093202ba48353f07074fec6d0`  
		Last Modified: Tue, 06 Aug 2024 23:57:40 GMT  
		Size: 20.1 KB (20069 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:b1cf08e618ac309a00ec6e2f070a9bcd3cc23208e274a26576f331cdaec8f8f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78681391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e55dcbd5c1075df5834c467a803d4192b047a604d35f7704c2bf737e815db4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOLANG_VERSION=1.22.6
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
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccab56a7828fccbfbf3c5386b666669245e0d8f93e53acce7ed8222093ae62a`  
		Last Modified: Tue, 06 Aug 2024 23:54:15 GMT  
		Size: 291.8 KB (291782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf2140beb75accb04ebf2792e51b647ea7478d06fdfc61e899388c6557ea6c8`  
		Last Modified: Tue, 06 Aug 2024 23:54:17 GMT  
		Size: 67.7 MB (67728907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d717ed77f52ec8dd7e545c08d89595a7b031b2a0a2f88b4508c8b8af9ad509`  
		Last Modified: Tue, 06 Aug 2024 23:54:15 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fcd3a14d6d05037b1f4eca2e4d4bab9b7ee25486510f895fc0060d8f7709c7`  
		Last Modified: Wed, 07 Aug 2024 00:51:58 GMT  
		Size: 5.9 MB (5871106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a92e0d2204b0a7902ab795dbfaeee8cd7829788e846bac3be9c707b8cbf77d0`  
		Last Modified: Wed, 07 Aug 2024 00:51:58 GMT  
		Size: 1.4 MB (1423813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43a2f16d60ac0fd66dfc1d1f9601a339ca137421c242de5824266684a297f83`  
		Last Modified: Wed, 07 Aug 2024 00:51:58 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:4e5f5234a67cdd459ca0382f4634034a2364b339f8a6a37211d27fb5452820f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25cf29d4db012dce6b9f52f81f385bc33308756dfc71cd0287b0bcd69942e56`

```dockerfile
```

-	Layers:
	-	`sha256:f6c8930e4e20f13c6997a41e9f8f901cba185f46d9ea3bc7ae26a6d3cc75584f`  
		Last Modified: Wed, 07 Aug 2024 00:51:57 GMT  
		Size: 20.0 KB (20001 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:ec7631b4bff06eb92e20b78d8e5c5bf079bcd048e43196786bf0cbef582ae743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77890412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc6171692c6e372c657256a9e1ebcd2e64d7a986595671b3ef4a3b417a8e9730`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOLANG_VERSION=1.22.6
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
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c7318d3e5485ead98a8a7ffd1815df0d57c2d4e91ee5f14b79d688de1ab2cd`  
		Last Modified: Wed, 07 Aug 2024 00:10:33 GMT  
		Size: 291.0 KB (290953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38353948ef7c4a85c3e42510197b5f321621d39f3094140f1496e3ba11d3156a`  
		Last Modified: Wed, 07 Aug 2024 00:08:57 GMT  
		Size: 67.7 MB (67728993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1e91c8c77a2673696ef7af8b778c14360bd4f987ac60f54ab9ed14d3768e1b`  
		Last Modified: Wed, 07 Aug 2024 00:10:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec94c3bda33fbafd4ef12c0a86ca1dd3b5005379d1053526f80f4b68fc53c736`  
		Last Modified: Wed, 07 Aug 2024 00:52:09 GMT  
		Size: 5.4 MB (5354146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2301a39af05e4c38b1d7efeca9b92551fe60812c0c5b590fedc926da8b7e27c2`  
		Last Modified: Wed, 07 Aug 2024 00:52:09 GMT  
		Size: 1.4 MB (1420769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0136faf96c1aae7a300bd0ade54687b7fbcf932ac77953cf351026d83c5f04f3`  
		Last Modified: Wed, 07 Aug 2024 00:52:08 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:964d6f6f8678962fd287e78c205b4cc3b84eb6699eae8402cf468a62fee02608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.7 KB (309685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb93cae37b564c15d21f5b8c2bc481a761e849fc252be748eeba35812e59f4f`

```dockerfile
```

-	Layers:
	-	`sha256:bc8bc47af41521c2f8a922043dbe0898b0b991d40e8246dd6dfd68ddaedf986c`  
		Last Modified: Wed, 07 Aug 2024 00:52:08 GMT  
		Size: 289.5 KB (289465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d131b8953e28798b5a9fa6d5549ad002b3abfc43212d2af9df59cb6ff8d13535`  
		Last Modified: Wed, 07 Aug 2024 00:52:08 GMT  
		Size: 20.2 KB (20220 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:ecfb07973f33e6466994dcfaea899b416d5ae6686ff53c5f5389fe2ac0bcb5d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78101315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a360febb6209e0c4417ff18860d940024c7708f4d6dd17470bc9c7f650281bde`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOLANG_VERSION=1.22.6
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
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171883aaf475f5dea5723bb43248d9cf3f3c3a7cf5927947a8bed4836bbccb62`  
		Last Modified: Tue, 06 Aug 2024 22:57:38 GMT  
		Size: 293.5 KB (293514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6edaf09ec107de8a2f93a55fc7fad71182aeefb0572c5f2e2f498d1ab1fd3b77`  
		Last Modified: Tue, 06 Aug 2024 22:56:17 GMT  
		Size: 66.3 MB (66283242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a0e5a2171f585d8583eaa13b4880bcb5ec9d3d2575d3d4fdaa6a24186c703e`  
		Last Modified: Tue, 06 Aug 2024 22:57:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e816dfc622365425863b049310fb33d8e956264cd5b5e5045c9b8fd418d77664`  
		Last Modified: Wed, 07 Aug 2024 00:02:57 GMT  
		Size: 6.0 MB (6039863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24257d431aa6bd1d42a73372a7eeccf04becaaa7550d4092ee50645182a0df2e`  
		Last Modified: Wed, 07 Aug 2024 00:02:57 GMT  
		Size: 1.4 MB (1397170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed75c71303ea781e88d9c3cc1277bbb872599a755f25a262c087c5ce3f828e9`  
		Last Modified: Wed, 07 Aug 2024 00:02:57 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:cb2beb5f0ce4aea4dd41eb569f44a0444bfd28377700a3091cc0a132c16e853b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.2 KB (307202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ddfe955b676a797694d8bfd4543ada07c8c3ea3f003854db51d692f50a130d`

```dockerfile
```

-	Layers:
	-	`sha256:d36c996eae14eb136cc0140b9c438a5a0f9ff9ad00d205e96c3c9a086e6f3a85`  
		Last Modified: Wed, 07 Aug 2024 00:02:57 GMT  
		Size: 286.7 KB (286671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1c4bdf7c67e8db1b8abee76c8115b4245d4ec606641b36bdaae46e5a26b039b`  
		Last Modified: Wed, 07 Aug 2024 00:02:56 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:4f7982c6a592456f14baad9f813e5c86080e5d07fd5a2f4660e5ef764e6b7f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77954223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5c32e92b9d451b8b8cde81b8b5fcf9295f6f97922412ec3dfd07965aadac03`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOLANG_VERSION=1.22.6
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
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3799a78dfbed4f51d46b0331c523ca613f2dab716b4caeac0e3c3fc3a052197`  
		Last Modified: Tue, 06 Aug 2024 22:59:30 GMT  
		Size: 294.0 KB (294033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa907a73ecb9721e6fd07eeff45b3daafd73705b1b26a4ab050075d2da72289`  
		Last Modified: Tue, 06 Aug 2024 22:57:05 GMT  
		Size: 66.5 MB (66453881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3880e24cd21f53fd75298cf317970da7e553a2560ba8a3ef4724e2cee96c8971`  
		Last Modified: Tue, 06 Aug 2024 22:59:30 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13dae48034d79840624ccf4a0809ba64289dcb832985e6ae179c46b92443b43`  
		Last Modified: Wed, 07 Aug 2024 00:00:02 GMT  
		Size: 6.2 MB (6244130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736835287d952ebe896bb137001036a64fe29cac26aeba823f8c252bf44bd3e2`  
		Last Modified: Wed, 07 Aug 2024 00:00:02 GMT  
		Size: 1.4 MB (1390031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0973d4689cd278dc817d9621e9cc82f0b94c6a4d0716f589032e28b8f3f750f`  
		Last Modified: Wed, 07 Aug 2024 00:00:01 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:da953fcbc39c7c70a23cdb4ab8d86a3230dbe06c9421540a85e4064408c01d5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.9 KB (304873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917eb23d62f68d3c46e8f91ae0f68fc69c36e86f3bec48f2dda7ab47361d108a`

```dockerfile
```

-	Layers:
	-	`sha256:d904c53b93f199604c0a44591445011385a739fd09f17d17fd6f011c4fff3e30`  
		Last Modified: Wed, 07 Aug 2024 00:00:02 GMT  
		Size: 284.7 KB (284705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a8dc469058601a5a921d26a4a0cf88a0beddc11ade1929885135ea7a5205a72`  
		Last Modified: Wed, 07 Aug 2024 00:00:01 GMT  
		Size: 20.2 KB (20168 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:125574500f903e9df0ac7766a1fffcf12b617985e111205b536e44b2a341b3fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78111852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79ab0e6b1dd4a3362d42e84829e9b8e9088d504a017db372d4d0fb3f36aa39fc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOLANG_VERSION=1.22.6
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
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a571abf33b31d34423d7fdec7f124b736d3b8c4bf672ec686abf087f11f88a`  
		Last Modified: Tue, 06 Aug 2024 23:01:07 GMT  
		Size: 291.7 KB (291678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d8e666b8b6272ce9413619cc27a5e9cc1281ec6e647ff787282c5aca125bd9`  
		Last Modified: Tue, 06 Aug 2024 23:01:16 GMT  
		Size: 66.9 MB (66907327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4d3ad1bdd0060586f7ea3c5214bf71adb3bd8d05a080137f9d2af51c3a0a50`  
		Last Modified: Tue, 06 Aug 2024 23:01:06 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4976bd908ae87ebcdcbb346cb62a2f432978da8765995ef9d312e4c38ea9d030`  
		Last Modified: Wed, 07 Aug 2024 00:13:51 GMT  
		Size: 6.1 MB (6137286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66ffcd32801b431f2678fb0921ef27ec8efbbf07c3d96328198d152e2181219`  
		Last Modified: Wed, 07 Aug 2024 00:13:50 GMT  
		Size: 1.4 MB (1404296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62911d122ab53ee6315dc9b60007706cfb365e018ba11f005a4205a63e443a0b`  
		Last Modified: Wed, 07 Aug 2024 00:13:50 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:d6fcf552a2a1ecf5ae53f581a5fc847e4059df49db3af27bc8887e6bb4451008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.9 KB (304869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b7e368b94e11389c7ab2c9f4b2eae9407c3c15278d418e49bfd92775b946f8`

```dockerfile
```

-	Layers:
	-	`sha256:d80e283bba96400e8c51e6e42bd3f710740f20919cbb619ccf5ed68fe2800869`  
		Last Modified: Wed, 07 Aug 2024 00:13:50 GMT  
		Size: 284.7 KB (284701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c235aba8a726074b34096e7579159b545e08eb03b60d28f64159ba37ff6f1355`  
		Last Modified: Wed, 07 Aug 2024 00:13:50 GMT  
		Size: 20.2 KB (20168 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:f902812dc65067d1813dc4e8503ece93952b749769d7ce36fcbb35318e4ff328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79809532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7ad32271f1973e2b4a023854ee0cd2a1565562d897046cbfffbd3b248ca183f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOLANG_VERSION=1.22.6
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
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c54ba5fba90bd52699c553f5c39c0b0ea45ac64b4d9ca09afb762001ab7bb6`  
		Last Modified: Wed, 07 Aug 2024 02:05:20 GMT  
		Size: 291.9 KB (291897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4f522c886389638258537d7ed45e62dbad030e5ed340cd291df30569fc9288`  
		Last Modified: Wed, 07 Aug 2024 01:54:06 GMT  
		Size: 68.4 MB (68420968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb91573b6ad53e5d8adc574aa13f3ecfdddb6225be1b5de558a4c4a087b2f23`  
		Last Modified: Wed, 07 Aug 2024 02:05:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc43e8c2afb2041f408f15e70c29a5d50b9cf096785fc3c1a63ded1c31d314f`  
		Last Modified: Wed, 07 Aug 2024 08:54:45 GMT  
		Size: 6.2 MB (6183225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157dd6173cb650edc8e3d536b064d9568ab0000e8210e2752a37c21eeb43a530`  
		Last Modified: Wed, 07 Aug 2024 08:54:45 GMT  
		Size: 1.5 MB (1451785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608daa3a3685d9217f109c7a99c51aff5c4585e75baac79781fd0610041ff840`  
		Last Modified: Wed, 07 Aug 2024 08:54:45 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:06194f1ad65f53794789ae51f6425d8c9956180f3f58144bc1633fadb37f36a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.7 KB (304712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18f310975d32de260453107466e0998c695bb70bc279f6abcf210bc2dc9c31d2`

```dockerfile
```

-	Layers:
	-	`sha256:43e9dbcb7f5d1c807a8ffa3c821a1889b3edc88ff79ab52bf36b9b5feb074a78`  
		Last Modified: Wed, 07 Aug 2024 08:54:45 GMT  
		Size: 284.6 KB (284613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0390abbe71e7678d8cf0e7984d408d5d77b8992d3bd9091241a610f866cd69a`  
		Last Modified: Wed, 07 Aug 2024 08:54:45 GMT  
		Size: 20.1 KB (20099 bytes)  
		MIME: application/vnd.in-toto+json
