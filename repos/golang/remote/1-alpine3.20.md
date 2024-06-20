## `golang:1-alpine3.20`

```console
$ docker pull golang@sha256:f46eb222fb7fcd330618499eddef228fdc1be9b7eb2490d37139797e7e33ca38
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

### `golang:1-alpine3.20` - linux; amd64

```console
$ docker pull golang@sha256:5c026b4c2a65d2edfb2cc15540ebea7c00351505691af0714af9f3dc140926a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73260214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288827cf059ed530cf2400518e01f3841781c178c483ecbe1be7816efb581aa7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b732c871fea20cea9c9afe0ee6c127852025cd9f1119819121110f1838b304c`  
		Last Modified: Fri, 14 Jun 2024 17:54:03 GMT  
		Size: 292.4 KB (292416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060aaf7efd0676cdf56165fe26e63a047d7f3c483ab1043d530db9370e6c28e7`  
		Last Modified: Fri, 14 Jun 2024 17:54:07 GMT  
		Size: 69.3 MB (69345548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1964877d6860798d7794738b2706190a440706bbffacdaea35594d1ddac0fc`  
		Last Modified: Fri, 14 Jun 2024 17:54:03 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:73cb6d93d8318a4c185e7eb96c5ea9414e756264450e781ec4584b3a06ffb8ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3c0ffb4ea70ccf375e229664bb9d8b33241d40c6fcf8c4f30157d6d0c8a345`

```dockerfile
```

-	Layers:
	-	`sha256:2c06e1b9f6a39d0eacc418ad6bcb610c922d2ac8e42ba77e8ad50a287c3d7585`  
		Last Modified: Fri, 14 Jun 2024 17:54:05 GMT  
		Size: 25.6 KB (25624 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; arm variant v6

```console
$ docker pull golang@sha256:9b3328fe61d3d4c54a66fbe0f7a4299e3eed8d57dee5800e5e21dc31b52efcf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71372132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf4ff6c2c8cf729bab1433aeafdec464035a2a24e45440426d19916e6bc4677`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
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
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c441603d6549470641a32cf5009fe72981601d1e7b487b889cc4020c08b00465`  
		Last Modified: Fri, 14 Jun 2024 20:04:01 GMT  
		Size: 293.6 KB (293624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743e448a2b4bba38b1783fb849b3f5093e7931cf69d898520c4f1462ad93a836`  
		Last Modified: Fri, 14 Jun 2024 20:04:04 GMT  
		Size: 67.7 MB (67713294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d5604e05347ed6f8103c47b3238b65862397605d0c89a10a510426d4633698`  
		Last Modified: Fri, 14 Jun 2024 20:04:01 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:fa661c01b978803e51277e681cf4b59fa858b248bcfef92a507ac1898484a972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 KB (25752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ac9e4def5da08513d4a9b776b8e3a188aa333dab8965de42bf0dfcf635f010`

```dockerfile
```

-	Layers:
	-	`sha256:e7b43d99c9bc99eb7d2cf572ab893d87da6eeb67aecb5120e0f81c75ad8d6b53`  
		Last Modified: Fri, 14 Jun 2024 20:04:01 GMT  
		Size: 25.8 KB (25752 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; arm variant v7

```console
$ docker pull golang@sha256:dbea7d34854a5f399fd90f9ed23b03b9b10f60af97fc7c4f8c46bab4df473c8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71100060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3397a96f35545e85908182debdb578d4065e2e0dd5b8a3d423b7ec4b8a31ca3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
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
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f0fec4aa5208228cdd97142cd6f1bcef97090cb45801ea77c0386c3d9d0f9a`  
		Last Modified: Tue, 04 Jun 2024 20:22:09 GMT  
		Size: 292.5 KB (292456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8d8376f429e08832ffbb91ed771b1b953556865415b4e4c37033a89a2f8aca`  
		Last Modified: Fri, 14 Jun 2024 17:54:08 GMT  
		Size: 67.7 MB (67713411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c2b8aade3e7f812acd81e815726960c5d479cf6fa0a3c61e9db95ccb506606`  
		Last Modified: Fri, 14 Jun 2024 17:55:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:0bd0c0f02ae58e7f2d7c6f638e2afce1707741c389cedf489cba4c719edb1207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 KB (25751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a24a8a72d13402c5c6d31b93e5d6fa6151b81db0c8eafef147b5f25b53d6f6df`

```dockerfile
```

-	Layers:
	-	`sha256:c5569cfa659558ebf2b0d1161c4c69561ca5c474ba2a26e7812b35d68ace43c2`  
		Last Modified: Fri, 14 Jun 2024 17:55:55 GMT  
		Size: 25.8 KB (25751 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:05ad24f1f432e12a11a5898b2e51f114dac5ef2444feccdcb30bd077fe5b0edf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70652702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ae941743a26c8c86b717bd6b061b2adbcf9e88db898103a6941371cde65bcb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
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
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1415b17371e9e60943269f29a4d23a5e3704ddbc1ab4546289828f84c8f85ba`  
		Last Modified: Tue, 04 Jun 2024 20:21:10 GMT  
		Size: 295.4 KB (295442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2259e4bd2629c850a0f37f6d3351f44770f5d4afee65aac3cddcb3bf2a735031`  
		Last Modified: Fri, 14 Jun 2024 19:43:41 GMT  
		Size: 66.3 MB (66270325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6d2a831dd7403b4b795f9ffc9c489112103cd1c39d712070bd63a87b2f4368`  
		Last Modified: Fri, 14 Jun 2024 19:48:08 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:56c476c919fa2d4b89fd458f0a6f5e63596a4a4f857f2af8029a6ab5de87067c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (25972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de584ad87f66729b7768824f08025adada5c3414d5163450a4049179d91d700`

```dockerfile
```

-	Layers:
	-	`sha256:e50086da127e738d78b5032fe324559613cf21b52781449462206f9c84f2aa4e`  
		Last Modified: Fri, 14 Jun 2024 19:48:08 GMT  
		Size: 26.0 KB (25972 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; 386

```console
$ docker pull golang@sha256:33e46b7613e65c58b33b84873bbf23e33616a6a0cacd0b5fd9f06b446a2765b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71107025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff18d154be292a3f0cef04e34345372a16244be5f9b0f7e44abe6d8f98cc1b82`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 13 Jun 2024 20:46:13 GMT
ADD file:cd0e8f9dc9e579bd0c884d2c92e4773391bd73d8302d6f4a9bca0796e7ff9a77 in / 
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
	-	`sha256:354eb832d25d95145569d0a3a573fb95b8350ee897d5b90a2f67ec1157706ec2`  
		Last Modified: Thu, 20 Jun 2024 17:38:50 GMT  
		Size: 3.5 MB (3469470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77cf9d7129e3b7a6e7ee91c59691980de1cbfc06b9b3e55f2a5dda0a25ac9c6f`  
		Last Modified: Thu, 20 Jun 2024 18:53:24 GMT  
		Size: 292.9 KB (292878 bytes)  
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

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:5a82ce6b6b612e8564901e184169ceec0dc20d4bf917faceaec0bb361e293145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b647ee2d0e26014ddd4fe948d9e9371c9f1fca7a2568b2e04b0e92792f90d1a`

```dockerfile
```

-	Layers:
	-	`sha256:e4d0e4586a7d00f407de97fd208bcd4e8dddb5f83a3e86fae3ac83ebeb99efdf`  
		Last Modified: Thu, 20 Jun 2024 18:53:24 GMT  
		Size: 25.6 KB (25571 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; ppc64le

```console
$ docker pull golang@sha256:0dbb20871b26844dd3ac66ab67f5712c0acdc6553dea6409cec84e2929e67605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70306719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:132257498ebab4bde2eb7eb1de4a588230d33fcf7b4995afc89ab5e7be7fdca0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
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
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d80f5a26e017a5de387ee9062b6045acd39de2769d99f89412d8bf3a06a818e`  
		Last Modified: Tue, 04 Jun 2024 20:22:25 GMT  
		Size: 295.9 KB (295901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2210b2be98c546d98d20cd631f014745f73d191238d22c5e439478550b6727b8`  
		Last Modified: Fri, 14 Jun 2024 17:54:36 GMT  
		Size: 66.4 MB (66440814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee1536d69e63886254422ef719cbfc05e944ac23de507c77bde7e1190b6bb79`  
		Last Modified: Fri, 14 Jun 2024 17:56:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:d79731f5de45aa183c7984155eeb4e26e8ac4a6d88958d18984b814befc5a08f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 KB (25690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f99560da662603bf8869e8891ec2d54abc5f5ca3b2ce6a3372e0d57a1dabde1`

```dockerfile
```

-	Layers:
	-	`sha256:b8cfcc50854bcbaba968995365b4562b78702220ac6deaf4fffff59c50379668`  
		Last Modified: Fri, 14 Jun 2024 17:56:34 GMT  
		Size: 25.7 KB (25690 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; riscv64

```console
$ docker pull golang@sha256:9404262844440618615c14a078836662b83d7beec6c36a98a09e8971e9bd1027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70555236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5990591af05bea57ad81712748b92d9d711260a156b902b53877a0d44017d8aa`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 17:57:29 GMT
ADD file:adedc612a3543e3a541be8e74c994fc3782e0f4a762ca77a1e29e6abfc81d7d8 in / 
# Wed, 22 May 2024 17:57:29 GMT
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
	-	`sha256:f280e85d15153a8f10f3fa47dd9d639e7a8fc6c1c8795d7123a32a0c36f16f55`  
		Last Modified: Wed, 22 May 2024 17:57:48 GMT  
		Size: 3.4 MB (3368560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6846326a7435bb0812f1761b4d68193b8d5cb1f1bdcdf10bad75ac8e83ec7dfd`  
		Last Modified: Fri, 14 Jun 2024 17:57:15 GMT  
		Size: 293.2 KB (293167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720f2671938fbfe8609ea6b3e22d6f25d4497370e3b0109cc065588d36d42db6`  
		Last Modified: Fri, 14 Jun 2024 17:57:25 GMT  
		Size: 66.9 MB (66893351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c29b40752516671457ed4df74ab1914a01f46486d62b3d38f6ed1151cef79f8`  
		Last Modified: Fri, 14 Jun 2024 17:57:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:bb75836330b6aa9a4b0b70dd050520dd6d2ea9b357b9dfcdf3a1f333144fde7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 KB (25690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63f2eca6cb271b7c85ca62c172b33994f9e2a6b71f190fbfd3c3a7d08fdea37`

```dockerfile
```

-	Layers:
	-	`sha256:5e9735a114c07c3340a802dfcf5292bcd384c5118dce610662424806f1dafbda`  
		Last Modified: Fri, 14 Jun 2024 17:57:15 GMT  
		Size: 25.7 KB (25690 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; s390x

```console
$ docker pull golang@sha256:3d80e1af89867acb74e3da2ade248f4a4ffe40be113de4c2e4e79e38fd6787d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72159125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5b375d807dd4391188f9096dc3ae0e1a343dde55be4a7faee05d0799760efa9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
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
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de2e843de006048b62d6b06bfc83cfa81a3d30ed58401daa91927b1294d4a31`  
		Last Modified: Tue, 04 Jun 2024 20:25:29 GMT  
		Size: 293.4 KB (293405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54ac55846ff64482893d22cd74289e959d60007f939ee44a6905370f9611de2`  
		Last Modified: Fri, 14 Jun 2024 19:31:27 GMT  
		Size: 68.4 MB (68405222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f410bf0e354fc721a933146ceb370df116e2090b95760ab8137d4438566078`  
		Last Modified: Fri, 14 Jun 2024 19:37:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:6fa557d1f5e839afe108874bd9801f1eeef20c62c051d29e3d952637bc1ceb7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:245a3b594bb00b5220822be4c59c7928c7f74fb789d3fa681c5a63807047b5da`

```dockerfile
```

-	Layers:
	-	`sha256:610009c165af5b3d19d005cf6c1e79db44c3fa401ee5604852995923414cce32`  
		Last Modified: Fri, 14 Jun 2024 19:37:56 GMT  
		Size: 25.6 KB (25624 bytes)  
		MIME: application/vnd.in-toto+json
