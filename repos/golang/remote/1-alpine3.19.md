## `golang:1-alpine3.19`

```console
$ docker pull golang@sha256:a76e1ac0dd57619a48bc7ebced2a46c63160f78d84c1b1659bb414788cb0dbf2
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
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:1-alpine3.19` - linux; amd64

```console
$ docker pull golang@sha256:d87558ea5ccfcf09ff62b08d3e5a1e1d7256499ee4d1aeb22a75da56fb5d6ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73055904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55982048fb390b60b3e1469287a7a1e7d40967ffeae131c485e5821cd0a1a3d2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 13 Jun 2024 20:46:13 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Thu, 13 Jun 2024 20:46:13 GMT
CMD ["/bin/sh"]
# Thu, 13 Jun 2024 20:46:13 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOLANG_VERSION=1.22.4
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOPATH=/go
# Thu, 13 Jun 2024 20:46:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 20:46:13 GMT
COPY /target/ / # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4de722c63677a3cb7de14a6cbdaf9043d39e6b04eed0de075845d2f5535212`  
		Last Modified: Thu, 20 Jun 2024 20:54:51 GMT  
		Size: 292.9 KB (292866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060aaf7efd0676cdf56165fe26e63a047d7f3c483ab1043d530db9370e6c28e7`  
		Last Modified: Fri, 14 Jun 2024 17:54:07 GMT  
		Size: 69.3 MB (69345548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce10fef440a218a76ab1d8203843a40830993256b99bc45acc4daf70e0a506d`  
		Last Modified: Thu, 20 Jun 2024 20:54:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:3bb70e2a6d2d1b3243d136a811f4d82cc1d4dbe94e6e0ddb4cd302779cbf3432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821a7a72e7562a06121ded41ad097309e57efd343546b5bb33123906aa89487b`

```dockerfile
```

-	Layers:
	-	`sha256:3e50f37eb3f93e6224d5551bdd9c33e149394db0a4cde4874dafe2992c16be8a`  
		Last Modified: Thu, 20 Jun 2024 20:54:51 GMT  
		Size: 24.4 KB (24404 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.19` - linux; arm variant v6

```console
$ docker pull golang@sha256:662638e92a5c39350729b2be11ca694da28593a9e8b37e99ee51b690633707fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71173175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d6a4fc776d29d23de063143d8d49efbe9bb80113820216b7a68c039174ad60a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Thu, 13 Jun 2024 20:46:13 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOLANG_VERSION=1.22.4
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOPATH=/go
# Thu, 13 Jun 2024 20:46:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 20:46:13 GMT
COPY /target/ / # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21609836efaae1ff6cb42fc59040340f85a4714d00ba4f14b7c947e5d8e48f21`  
		Last Modified: Fri, 14 Jun 2024 20:04:57 GMT  
		Size: 294.3 KB (294327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743e448a2b4bba38b1783fb849b3f5093e7931cf69d898520c4f1462ad93a836`  
		Last Modified: Fri, 14 Jun 2024 20:04:04 GMT  
		Size: 67.7 MB (67713294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddfa5be785c78954331cfad9e784be8fbc614b89f1e1bbb0e319474628ace347`  
		Last Modified: Fri, 14 Jun 2024 20:04:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:9d82e858091ef6b38e1c76d96ab0296299109216b0ab27b0a8c835476f8572f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 KB (24500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8b921a7b40936d3f120e2af7c564afb09db2f51882b3e8515daabbb0d133e1`

```dockerfile
```

-	Layers:
	-	`sha256:c0a4eabd4573d6ff52c5bbd1c2c28e5ac284cf9de056fb70e216157728128bd8`  
		Last Modified: Fri, 14 Jun 2024 20:04:57 GMT  
		Size: 24.5 KB (24500 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.19` - linux; arm variant v7

```console
$ docker pull golang@sha256:060ebc35673a949d41d90d26c07fdbe1813b04bd4e289d0d1832a2bf425d1a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70925644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a2b71aec6f6db06dffda6eb7b0f98d16fd1f72af36f90d573626c45e8157f6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Thu, 13 Jun 2024 20:46:13 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOLANG_VERSION=1.22.4
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOPATH=/go
# Thu, 13 Jun 2024 20:46:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 20:46:13 GMT
COPY /target/ / # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b70cb88bdc595e4a85eaf8f7d822f8d6bd3eda67539f21306737df618eb5d71`  
		Last Modified: Fri, 14 Jun 2024 17:56:25 GMT  
		Size: 293.2 KB (293176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8d8376f429e08832ffbb91ed771b1b953556865415b4e4c37033a89a2f8aca`  
		Last Modified: Fri, 14 Jun 2024 17:54:08 GMT  
		Size: 67.7 MB (67713411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fe7b442415918c60751ea19f1b34845202daafe7721bd8e9c001aa59c10de2`  
		Last Modified: Fri, 14 Jun 2024 17:56:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:6b20849ebd4e6e4cbd9c34e2fb2d43400de145fd4937e728dbab611564e45995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 KB (24500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45157c1b2590e6d5b0878dd858add3260f79344260a2fa264da192821a206514`

```dockerfile
```

-	Layers:
	-	`sha256:e5e0eeffe06a76e7c94eaf2c4b002b1b1d9f8d4225582deedbccf6ffa02c7527`  
		Last Modified: Fri, 14 Jun 2024 17:56:25 GMT  
		Size: 24.5 KB (24500 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:f9bb069511874508351aacde765715fd79b08e839e3aa59c912a8a57079fe843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69914262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e10700beaef7ae0eb89ba8f1ea556cc9a691c9ec736b506236193cf251828f7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 13 Jun 2024 20:46:13 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOLANG_VERSION=1.22.4
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOPATH=/go
# Thu, 13 Jun 2024 20:46:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 20:46:13 GMT
COPY /target/ / # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c02a022ea09ee057438ef30f00cf15df535805b2e552ec533c95f7ecbef4c62`  
		Last Modified: Fri, 14 Jun 2024 19:48:36 GMT  
		Size: 296.1 KB (296064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2259e4bd2629c850a0f37f6d3351f44770f5d4afee65aac3cddcb3bf2a735031`  
		Last Modified: Fri, 14 Jun 2024 19:43:41 GMT  
		Size: 66.3 MB (66270325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583b06541e1613cb09e7c87e84d62db934de006144cc2abf72adf2b2042b20c8`  
		Last Modified: Fri, 14 Jun 2024 19:48:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:89e29cbfd2b408c5a55e57f07acd812c0e508eb84b19ddbb031787385a872c74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 KB (24704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:644998078e689cbd72aa0f8145a521edcd07933227a7710e0266edf96ed38057`

```dockerfile
```

-	Layers:
	-	`sha256:eb24457f9fa0e3d433e9d0b383a2963334d89248f787c9a21614992e0f8ef246`  
		Last Modified: Fri, 14 Jun 2024 19:48:35 GMT  
		Size: 24.7 KB (24704 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.19` - linux; 386

```console
$ docker pull golang@sha256:b923d0f43e8bc004ada045de228ec1872e23fcc0b41912f40e77ecfae56a44a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70889076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cbae27d6d3d512f117ed4e181655f0c012d21f0c73c74d6b453ac5c7f15757d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 13 Jun 2024 20:46:13 GMT
ADD file:fef5870f3bb90ed437c0331d7e65e52da6728b66d231aea95a605935fef056d7 in / 
# Thu, 13 Jun 2024 20:46:13 GMT
CMD ["/bin/sh"]
# Thu, 13 Jun 2024 20:46:13 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOLANG_VERSION=1.22.4
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOPATH=/go
# Thu, 13 Jun 2024 20:46:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 20:46:13 GMT
COPY /target/ / # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e9c6bf0d8f3154c26ee87ffe9feb02c91666069b8cbe0668cfae10922ad80c49`  
		Last Modified: Thu, 20 Jun 2024 17:39:06 GMT  
		Size: 3.3 MB (3250890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db8cb95d91efc458ef1e9d12124c370ee86484ead8e7101b844c06ced306f64`  
		Last Modified: Thu, 20 Jun 2024 18:53:24 GMT  
		Size: 293.5 KB (293509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d423f142b846e34cad754942d9961e223ceeaa092ba25d1bfbe95eb1364c405`  
		Last Modified: Fri, 14 Jun 2024 17:54:03 GMT  
		Size: 67.3 MB (67344518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9be4f0f2960b7c312aba0de8fc11e502c1e6ec8fb8afe41563ae8032a5523f`  
		Last Modified: Thu, 20 Jun 2024 18:53:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:e71fcd3b7ca931400ae60dd75329efbb64d421371367859c3587861dee489650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff664c7c9d7b0781069873b43fa3a400dc901447520b05200e4a254d7cc3daa`

```dockerfile
```

-	Layers:
	-	`sha256:22d7761d828372c2c8c67d64e97c587146de58dd93fff2952e6ddaa43c8697b1`  
		Last Modified: Thu, 20 Jun 2024 18:53:24 GMT  
		Size: 24.4 KB (24371 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.19` - linux; ppc64le

```console
$ docker pull golang@sha256:b393bc63bf4b90d9b4677ab4e7eefc304543e3f7f56a975f36421f710a8a5345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70098043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606222e69ae1d4fd0fcfbcd70e96a39e932dd214bc26ee403db4fbd504df572d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 13 Jun 2024 20:46:13 GMT
ADD file:2bbc16bd313a28bd824794768ca122cd630e13eb133abbc1945768f5fadb6afb in / 
# Thu, 13 Jun 2024 20:46:13 GMT
CMD ["/bin/sh"]
# Thu, 13 Jun 2024 20:46:13 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOLANG_VERSION=1.22.4
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOPATH=/go
# Thu, 13 Jun 2024 20:46:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 20:46:13 GMT
COPY /target/ / # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a87ce480a1e6b2a211e539793eb8993daec4a7b45a3b284a63476a172be632c2`  
		Last Modified: Thu, 20 Jun 2024 18:19:08 GMT  
		Size: 3.4 MB (3360635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74b945c556201ab5f517d3a20a28bb0cf28417cf00964d99472b33c0c890e8b`  
		Last Modified: Fri, 21 Jun 2024 01:48:40 GMT  
		Size: 296.4 KB (296435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2210b2be98c546d98d20cd631f014745f73d191238d22c5e439478550b6727b8`  
		Last Modified: Fri, 14 Jun 2024 17:54:36 GMT  
		Size: 66.4 MB (66440814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92159a2dfb816a26d382f6e46b5cf3c99c5498f9511ba49afaa5f58e4b77087`  
		Last Modified: Fri, 21 Jun 2024 01:48:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:756b44a37b5e4c73a4d678c09d4a0017c561ade763ec5ba72645d60c0f3a3d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2becbbf6a9bf401aa96992995927500bd56308105f221e9239c17c2f9d833a1`

```dockerfile
```

-	Layers:
	-	`sha256:fa06dba49cabaad4cf3afb4a2c7944c152b53252804ec9d14f7e9c6fab7ac2aa`  
		Last Modified: Fri, 21 Jun 2024 01:48:39 GMT  
		Size: 24.4 KB (24446 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.19` - linux; s390x

```console
$ docker pull golang@sha256:427524ab197294cfbb87c787995027db2e44f378b07787e511afef7ec20ef94f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71942120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fbc70421f61464421ae20a1c3ae7024c6dba41d20e0d0b2bfc098b39b38a49d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Thu, 13 Jun 2024 20:46:13 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOLANG_VERSION=1.22.4
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Jun 2024 20:46:13 GMT
ENV GOPATH=/go
# Thu, 13 Jun 2024 20:46:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 20:46:13 GMT
COPY /target/ / # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Jun 2024 20:46:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb46dd60a0721336f705bdefae11d144944f110896f69028fe18265d9b32ad7`  
		Last Modified: Fri, 14 Jun 2024 19:38:46 GMT  
		Size: 294.1 KB (294105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54ac55846ff64482893d22cd74289e959d60007f939ee44a6905370f9611de2`  
		Last Modified: Fri, 14 Jun 2024 19:31:27 GMT  
		Size: 68.4 MB (68405222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43574ceb5cbd1e5a492b67eeb7a196c9d04abe8b2a42dd2a6e06c8b57999d08b`  
		Last Modified: Fri, 14 Jun 2024 19:38:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.19` - unknown; unknown

```console
$ docker pull golang@sha256:8f7596563d18b098f55cf65bce260923323bb88c4d5f836233b51fa7a21390ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c713a5cb2fedc01ba070a0b00fa811904f62a324427285a4283b6ab1c3c835c`

```dockerfile
```

-	Layers:
	-	`sha256:60fb743aa3dea0c82375004d97eba430342af03710100340fe955faa161af93b`  
		Last Modified: Fri, 14 Jun 2024 19:38:46 GMT  
		Size: 24.4 KB (24404 bytes)  
		MIME: application/vnd.in-toto+json
