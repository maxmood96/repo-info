## `golang:1-alpine3.20`

```console
$ docker pull golang@sha256:1b455a3f7786e5765dbeb4f7ab32a36cdc0c3f4ddd35406606df612dc6e3269b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:1-alpine3.20` - linux; amd64

```console
$ docker pull golang@sha256:1bddfed44ff69c533c0ec006515afb7350986b0d7eb7383f780ab5525f4f06ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73257368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0594d7786b7ca10f1be62758b4f14a2c7d104de1977858d6aa20b1e076fa100a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a827483052c5871ed2242ec5abe36562565f754f5e9b34f4e27b49644d518015`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 292.4 KB (292420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b8906d0df87fe33fd7a8a6b4c4bfa7a02f1c28477f208b9a18dbd113a631fb`  
		Last Modified: Wed, 22 May 2024 22:55:58 GMT  
		Size: 69.3 MB (69342695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c56c33a8080322e40c97a0a37dfdfb7572e778302eb6bb89566112d3ee6d06d`  
		Last Modified: Wed, 22 May 2024 22:55:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:13210402d18f2c6a89eea7ff260c2b510644af46435318194001026305ba73eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 KB (23844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e17ab9ac2fc9ab2dea4b95a713101986545a3b726c44a259f3fc9c411aa9cec`

```dockerfile
```

-	Layers:
	-	`sha256:dd14b9784986b259e7e2d9089901de7031b8f51b6f1e2cbaf97112bd6c233816`  
		Last Modified: Wed, 22 May 2024 22:55:57 GMT  
		Size: 23.8 KB (23844 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:638709d35305a16b38f575eabe97e2cab3229169cf555ebd5e98630f794f595c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70654417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2a7462eb04ba6b0b64719de897a917431010ff74291ccd619423414cb62432`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fd4d77c1150ba7c64d2b9cb1ad73058c134eea51cdf8a7c969379c3fe358c3`  
		Last Modified: Thu, 23 May 2024 06:26:56 GMT  
		Size: 295.4 KB (295445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269d540c1f502e66badd39f9acbd5037011b4a4a15454c8fb22de7aa4378ae97`  
		Last Modified: Wed, 15 May 2024 09:08:33 GMT  
		Size: 66.3 MB (66272038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6930e6242b08ff7992e85b10519d54167d7ffdedf7199e086b7c8be95e4baf6`  
		Last Modified: Thu, 23 May 2024 06:26:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:e6feff72e44b3a90aa8df43db17606970ae86ea4d8bca7381ca36eb677e743ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 KB (23697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637e110c69f328847fe84b1f26b823ab5e6e042f6b2bb457ad84038824120a8c`

```dockerfile
```

-	Layers:
	-	`sha256:8c86a93f44580abb3028a08486875f6cb9bb717d1ef29872bc4601f93710047a`  
		Last Modified: Thu, 23 May 2024 06:26:55 GMT  
		Size: 23.7 KB (23697 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; 386

```console
$ docker pull golang@sha256:c22e3c6a61734265c5fa044b4feecdd14bfc0d02cf208a4028e05945b1742419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71103540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606b385368ef7601d908287957af6cb66bd7988b6d11c5d63c88a4b1e07ccbee`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5636e6cae80696e05367d32690db4a8577dd0a3c759d450e134975a03bbc5afc`  
		Last Modified: Wed, 22 May 2024 22:55:01 GMT  
		Size: 292.9 KB (292872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd3d68e21a67472f9828cf1f154f8f9b2784731bbf6c1491c371acb44f7e29a`  
		Last Modified: Wed, 22 May 2024 22:55:03 GMT  
		Size: 67.3 MB (67343328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2fb62a4ab8844a7f8050a32d3e249c3c80b3b0874cf190b814216d3afa68be`  
		Last Modified: Wed, 22 May 2024 22:55:00 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:bfb4dfa5dbbb979f9879f070472876c384231581c295fcc5a123eae6188aec95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 KB (23792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e1d1ace2ec5eb90227588b05427ec430439a71857eb7c704a9466a6ec669917`

```dockerfile
```

-	Layers:
	-	`sha256:a6708b731df9c47ff12e2d35730eb7e7cf00288cfe74bc572e047d761cbdfed8`  
		Last Modified: Wed, 22 May 2024 22:55:00 GMT  
		Size: 23.8 KB (23792 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; s390x

```console
$ docker pull golang@sha256:b121b1ec284faa85ddcb896865995c0a77e996172abda14b84bf44dfd16419ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72152978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48816ecd8dcd17e6434952e590b7f0e7022a0bbef3eb40d8777afc81ba8fd09d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e66d9c1932c81dc738c92566c80482d80ffdd93de4411f25e01523a5c4c859`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 293.4 KB (293402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2482b2ed92bc4103a166e8c33b88d4d23fd167f50526ca1710fcfd6050c54952`  
		Last Modified: Thu, 23 May 2024 03:14:14 GMT  
		Size: 68.4 MB (68399077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b16ac5f62001aa9fecfa7a1deaef728e369ce04bde6ae9c4ce50e5b79638a9`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:761a1ed8b6aff9e8d483d929102ec73068841012ed61fe2628c934c84759ac97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 KB (23678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0307bd9334a4fee50a3a69d740342df83ea43151ff5540cd0c3b23b33b6256b`

```dockerfile
```

-	Layers:
	-	`sha256:60936c9ad58ccacdceb9d0d6914fb9cba21551eccda9671ed296411cfac69dd8`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 23.7 KB (23678 bytes)  
		MIME: application/vnd.in-toto+json
