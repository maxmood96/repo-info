## `golang:alpine3.21`

```console
$ docker pull golang@sha256:b6224579413159e9d4e82e1f160e1e551e947c3fe79db50d1431678374c5dbef
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

### `golang:alpine3.21` - linux; amd64

```console
$ docker pull golang@sha256:c68fb23e94573004a99d7c5eab2dbaefeb81f56f13180568911e45cfc5b458c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77982619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:038b36ac86e1e1acca94944cdda3c1da21392d726a5ad31a09cecfa9c0277a4c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 18:26:14 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOLANG_VERSION=1.23.6
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOPATH=/go
# Tue, 04 Feb 2025 18:26:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 18:26:14 GMT
COPY /target/ / # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3a26c0c732c4b931d38761c5cb9be8f635c2712e5bd330ab4e061dd4fb3fbd`  
		Last Modified: Tue, 04 Feb 2025 19:32:45 GMT  
		Size: 294.9 KB (294891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd968b00abc2f44f5d74b014d2b833a05dd020b5f534f19dca853c409df33466`  
		Last Modified: Tue, 04 Feb 2025 19:32:46 GMT  
		Size: 74.0 MB (74045855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58be0b164ee7f3471be9e37bc9b9b41a91f4c6f81e5fe0381670a021ed8367e1`  
		Last Modified: Tue, 04 Feb 2025 19:32:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:e96c4d47e05245eae0e0f7bdcf37bd38f848b59fc920bcc3d3a0088a6f4b8b72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 KB (243047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9f748e8466d572c75c46fb0311b20caa2c48753b3def20e5291a4123d1c81b`

```dockerfile
```

-	Layers:
	-	`sha256:7812ccae61bf3e0629dd23c85b0edd924ffc7a4fae1a4aed649f938a10ef3532`  
		Last Modified: Tue, 04 Feb 2025 19:32:45 GMT  
		Size: 217.0 KB (216977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a117afd47906defe04f924c5fcde539a9504cab1059d235e9d0d3674ee8c0fd`  
		Last Modified: Tue, 04 Feb 2025 19:32:45 GMT  
		Size: 26.1 KB (26070 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.21` - linux; arm variant v6

```console
$ docker pull golang@sha256:0376b84d88e10a6695c55a5f98bb45946e989362913c9c6f74fe37b255c9584e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75855594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691c5bc659cee0f0266e88df435652db34731b4eab2f61f3a58065a31987b9f4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 18:26:14 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOLANG_VERSION=1.23.6
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOPATH=/go
# Tue, 04 Feb 2025 18:26:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 18:26:14 GMT
COPY /target/ / # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f03f69a8f388ed7361ffb2b4247b3a48f246dac506cf30e7f01c792fb81bc18`  
		Last Modified: Wed, 08 Jan 2025 21:49:41 GMT  
		Size: 296.2 KB (296242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7bc15bd6dff137475f22b6631116b4ea034384c5e21f31d1ca51949d8498e95`  
		Last Modified: Tue, 04 Feb 2025 19:33:14 GMT  
		Size: 72.2 MB (72195315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc50c5796c435c52117dcbd4851b161d2e05c503037fff587ed3f7cea78df074`  
		Last Modified: Tue, 04 Feb 2025 20:38:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:293c65eedc2f1df92cdeb9f33262c1797b726a87613a4443931cd02a809e5147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (25988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74e0285f03fdfca1965b950bbe225641e00aa82dde9e01f2dac69720737aa39`

```dockerfile
```

-	Layers:
	-	`sha256:2a6437d35e2366883c1c4a9cfe41895599dbbf87f32b6bf0b77486b58f43dbcb`  
		Last Modified: Tue, 04 Feb 2025 20:38:33 GMT  
		Size: 26.0 KB (25988 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.21` - linux; arm variant v7

```console
$ docker pull golang@sha256:de6b9de23c83565cc3c0145c1d4bb437a6fc37b0038bde56857afc1b12817e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75586370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ffafacc8c9d3baa067ddd12f521f2d6c07aa5380cfe2d0b8dfc4f575bcd2bec`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 21:14:07 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOLANG_VERSION=1.23.5
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOTOOLCHAIN=local
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOPATH=/go
# Thu, 16 Jan 2025 21:14:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Jan 2025 21:14:07 GMT
COPY /target/ / # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d0001409a747749230c7a654e2687c0848bbc83674d48cdc49a7ace1ecdd14`  
		Last Modified: Wed, 08 Jan 2025 21:54:51 GMT  
		Size: 295.2 KB (295180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71181da0f46bebe3348744084ada18c7bb3fc1a115b2faa229669f2846f8a617`  
		Last Modified: Thu, 16 Jan 2025 22:10:17 GMT  
		Size: 72.2 MB (72193920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b06860d892ad634c5f9bd1c004b2b10e5a6ccb5187376cdbaa5f0d45218529`  
		Last Modified: Thu, 16 Jan 2025 22:11:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:61216ce6853b67248ff886b032614dcefcefa11d8f5ff473d20403832ebf725d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 KB (243212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:408194b702c9776bb8202d2a98699ec976a43bc971d37e0ba0c40f0c2c62dc2b`

```dockerfile
```

-	Layers:
	-	`sha256:c905962c5c9c5d251e4df69577ac76467db310ff42cd27188d9474f278a04918`  
		Last Modified: Thu, 16 Jan 2025 22:11:38 GMT  
		Size: 217.0 KB (217009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75f0d2c4445306f4e64910a6e35215d2bf87069cd015aa9e34eb13f7dad4d4ee`  
		Last Modified: Thu, 16 Jan 2025 22:11:37 GMT  
		Size: 26.2 KB (26203 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:e8630f35a0930fb45171797c621b77d47315081c86ef0b9d5e6ac92fe580a620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74966660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec5d4cf8479eaf7d580ff5256466047ebf8ba3a59ff1d9c60225a3fb29a9527d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 21:14:07 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOLANG_VERSION=1.23.5
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOTOOLCHAIN=local
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOPATH=/go
# Thu, 16 Jan 2025 21:14:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Jan 2025 21:14:07 GMT
COPY /target/ / # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1056f4fea241387de443606efbb463ff34c3d723317da5aaff9ca1d42468d46e`  
		Last Modified: Thu, 16 Jan 2025 22:07:17 GMT  
		Size: 297.9 KB (297868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9d514b7aa85ba6aa1665a90e4a24f9a4312a9ae69f1e26235cf49d08b80c7b`  
		Last Modified: Thu, 16 Jan 2025 22:08:29 GMT  
		Size: 70.7 MB (70676275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f92ea2a58530aa31be3e611f075346f0aa7ba98cc5e5b792cd1dffe3e1650c0`  
		Last Modified: Thu, 16 Jan 2025 22:09:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:403f9fc4040de8d6184fc962ccc10ce2369dad173e5653e68e2e68899e13d382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 KB (243333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e727e09916bcfee4d21b0bd886d4180c1a0469b259c05ea0a34cdb1e18e7384d`

```dockerfile
```

-	Layers:
	-	`sha256:b8813d2c886c1c32b704bb76a6027deaf7471aabbc684af98d8d43003f79d62e`  
		Last Modified: Thu, 16 Jan 2025 22:09:24 GMT  
		Size: 217.1 KB (217081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c74aa740858508013834edd1956a952e9b2b3a3362ff9cfaf47729f910a73406`  
		Last Modified: Thu, 16 Jan 2025 22:09:24 GMT  
		Size: 26.3 KB (26252 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.21` - linux; 386

```console
$ docker pull golang@sha256:e7f52ea72d542675058efb09091941bd8ee8d805f15a77e50865231ccf02cae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75678683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac09b107a346d1c460da89f050fe4d81a86f884e097690c84a67681a3743a075`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 18:26:14 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOLANG_VERSION=1.23.6
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOPATH=/go
# Tue, 04 Feb 2025 18:26:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 18:26:14 GMT
COPY /target/ / # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab5771aa5e7366d75aaa4460b5fb91feb143e45ef0590756b917635c3ec2df3`  
		Last Modified: Tue, 04 Feb 2025 19:32:33 GMT  
		Size: 295.6 KB (295585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b77728945927969d0c8ded023b60910b4b7d2a79c658271ebe4948de9a6d578`  
		Last Modified: Tue, 04 Feb 2025 19:32:35 GMT  
		Size: 71.9 MB (71919814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ec68a51aa1bf567b3a1211fb344e50eccbc70e531a56c169d87070853dc2a0`  
		Last Modified: Tue, 04 Feb 2025 19:32:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:63d4f47338a290db3e93ea9ea2da2e80416129b781da23d7efbdd8fb03b790cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 KB (242909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1bafb80e6b57d8cd35ab8b9610392a3c62ff7c15dfaad83813143efa16751e`

```dockerfile
```

-	Layers:
	-	`sha256:ab700441b78fdb63d41799a4479714c7b91679eaa87dc196dad98cee712add3f`  
		Last Modified: Tue, 04 Feb 2025 19:32:33 GMT  
		Size: 216.9 KB (216896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:881e29a5223f4adfa846d1a5a9f906a70d5c0e92ff2479dedd4d7063c8144f0f`  
		Last Modified: Tue, 04 Feb 2025 19:32:33 GMT  
		Size: 26.0 KB (26013 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.21` - linux; ppc64le

```console
$ docker pull golang@sha256:2a18532bb2b200095872fff535343f5cb6761cec47611545b0db5abdb142345a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74710140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e0cfef877c0e9f61698d30d5d0be4a29d18c834b7fcd5e254194a6b886fed1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 18:26:14 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOLANG_VERSION=1.23.6
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOPATH=/go
# Tue, 04 Feb 2025 18:26:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 18:26:14 GMT
COPY /target/ / # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd68bfd3ee8de54b2fbc691d541267c5e55c57c253f41c0bd40aa2b5f9f17e9b`  
		Last Modified: Tue, 04 Feb 2025 22:35:27 GMT  
		Size: 298.3 KB (298275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76bc8515280eafb56fff5db8a8a3f9b1389a9563753c21ecf558291e30e86e2a`  
		Last Modified: Tue, 04 Feb 2025 22:34:44 GMT  
		Size: 70.8 MB (70838106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20538c90512e94a603dfd13e10a2b34094f4f991ec2e9b9c029f3fb887df0acd`  
		Last Modified: Tue, 04 Feb 2025 22:35:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:3721276bb9af806c191f11f23386026ab70e3fec15564c7e49cf07539abb92c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.3 KB (241262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1250a9590f34ee9494c5e8bd98c3e59b5e5b7fd9bba8b540a1dbacdf3223cd`

```dockerfile
```

-	Layers:
	-	`sha256:50a2e6be0a1422bef806b9bf61d5465c77451879f43ffd23a194f9597bcb2076`  
		Last Modified: Tue, 04 Feb 2025 22:35:27 GMT  
		Size: 215.1 KB (215120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31bee1aed3deb8e36c3d0a851d8fb3ae11fde08116ff8fec4f49ff086628d86a`  
		Last Modified: Tue, 04 Feb 2025 22:35:27 GMT  
		Size: 26.1 KB (26142 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.21` - linux; riscv64

```console
$ docker pull golang@sha256:175074cf9f8333eff8dc13e9366b9df9be73ac6eb3f5401103a82e3f53ba8def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74882179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea18aaea9181f4850a1fbe25cbf663781074c83e663ef5fb1596e3ad43f9b44`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 18:26:14 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOLANG_VERSION=1.23.6
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Feb 2025 18:26:14 GMT
ENV GOPATH=/go
# Tue, 04 Feb 2025 18:26:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 18:26:14 GMT
COPY /target/ / # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Feb 2025 18:26:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d26d7d7362ba90a5c2912b455128da725e739b7dbd70f75dc1091bfed8ea2d6`  
		Last Modified: Fri, 10 Jan 2025 16:32:59 GMT  
		Size: 295.4 KB (295361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bcbafcf86e581c838713d6aa93c05a7dd1d0a064c9bb430f1bc2e58c504369`  
		Last Modified: Tue, 04 Feb 2025 19:37:04 GMT  
		Size: 71.2 MB (71236403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e75f7cdb16bc8df9bc2b9178c93c6e5803f34f95d2c87546331c69c4a7e3af`  
		Last Modified: Tue, 04 Feb 2025 19:36:54 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:99f8679c5054f7aa4744204e1a72d15ab02b989b8f7c74b4197d0766a395dea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.3 KB (241258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ac1db8014f05a1f775f20ddd86054cf274e38412e3ddd3915ea15267a095b6`

```dockerfile
```

-	Layers:
	-	`sha256:44a88c6c580ff85ae3cac6523d0092bb024a0b4d75458cfc1c03ba9946832747`  
		Last Modified: Tue, 04 Feb 2025 19:36:54 GMT  
		Size: 215.1 KB (215116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1e3c5fc0d490f2cba9375d3f22ebb2a5394b8fef3e20ff36c67aef4b34db77c`  
		Last Modified: Tue, 04 Feb 2025 19:36:54 GMT  
		Size: 26.1 KB (26142 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.21` - linux; s390x

```console
$ docker pull golang@sha256:63fa31b48d84bfdba7c66d44059f9cde93baec9b7034c69bcd150db424dd7893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76717869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e8c0d773bd0cd68c6d28eb9b047763b4e8fd6712184c8102185eb4ec88fac7f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 21:14:07 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOLANG_VERSION=1.23.5
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOTOOLCHAIN=local
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOPATH=/go
# Thu, 16 Jan 2025 21:14:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Jan 2025 21:14:07 GMT
COPY /target/ / # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891798c8b7f45ed9fd4734da8ad75c1f6667b239c599c11f3cdab494a7a8406d`  
		Last Modified: Wed, 08 Jan 2025 22:06:35 GMT  
		Size: 296.2 KB (296160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b567a3d856120b002d262f7c532f30adaa977477b055fda3e7047c19dfbefeb`  
		Last Modified: Thu, 16 Jan 2025 22:11:06 GMT  
		Size: 73.0 MB (72954684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b192a56702bd3b84d700fd90816e66afc9c8d03959902eeddbf252c0b851dfe`  
		Last Modified: Thu, 16 Jan 2025 22:11:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:c6c861b892de6bd4e60dcf2c6604c694ce1be2f1c379c66af2355b4fc1514035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 KB (241096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e707112799db6c31a76af08d2040b57e3efe6d4ddc2c5e9b49d44624a92c62b2`

```dockerfile
```

-	Layers:
	-	`sha256:7d039e12737a84e7c400890d8e1dd09d17b01a27a5013fb2217b2cef22792d06`  
		Last Modified: Thu, 16 Jan 2025 22:11:55 GMT  
		Size: 215.0 KB (215026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8243c7bc1fb8275f3339789aa35e2b9ec8abb4ab3eb66a1a48c75bd8d79101e5`  
		Last Modified: Thu, 16 Jan 2025 22:11:55 GMT  
		Size: 26.1 KB (26070 bytes)  
		MIME: application/vnd.in-toto+json
