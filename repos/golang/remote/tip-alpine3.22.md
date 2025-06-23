## `golang:tip-alpine3.22`

```console
$ docker pull golang@sha256:38306f5a72c0a1ddb4e2d53104a93e201494ed8995fd73765753f22f6fd56397
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

### `golang:tip-alpine3.22` - linux; amd64

```console
$ docker pull golang@sha256:2073c0f887e0d0cd4c9defbb09c5b3dfaee95f6888889d713fda42b03f01572d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.3 MB (87285066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ec27f52fc1a91eead2ae2ea234254a3dadaa985350ee8fed3aec17c381926f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 23 Jun 2025 05:23:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 23 Jun 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Jun 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e0fb97e7021f4c61338170aebc3f058c8aec930c648e5bdde3e14b3c7faad7`  
		Last Modified: Mon, 23 Jun 2025 17:35:45 GMT  
		Size: 294.9 KB (294913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553943e6d01c9acd45d693254df521c1e8dd5f2af99f49bd85cc6c44cbb632b8`  
		Last Modified: Mon, 23 Jun 2025 17:35:46 GMT  
		Size: 83.2 MB (83193149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d141b25cf0d8979091b904dad3335d1893281bdda0ae9999bc0f1acc86ea65`  
		Last Modified: Mon, 23 Jun 2025 17:35:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:a96cc5e2399383ad8bbcff1b4259abb965e56f7a51d6334e989588bd0f61f831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.2 KB (221207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf41291ab7b878291df50b2ae4245527799440eaee16a4e1246151551ad9bc5`

```dockerfile
```

-	Layers:
	-	`sha256:3d4dcd7ee803d2cbff7af24013af4d97c08b8b636712f2a0c4cedbfc3b720193`  
		Last Modified: Mon, 23 Jun 2025 20:24:17 GMT  
		Size: 196.1 KB (196069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0015e894d5be0cad095a4e7585a5b0200d6fd12d4380b8ab9cb9b9e7ee3bc73f`  
		Last Modified: Mon, 23 Jun 2025 20:24:18 GMT  
		Size: 25.1 KB (25138 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v6

```console
$ docker pull golang@sha256:c8782f9d90190977629f5c79a73f9c460157fd206f7a8ecac1c31d145712117d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84320403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0bdd34c366765f8b6eea0cf18de8d7fad51a311e35ab4d14ad4c6e4ad9820d7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 23 Jun 2025 05:23:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 23 Jun 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Jun 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade1a66512d0d840a56a8c3fcd61678c4f71bc9949c18f7ee679feb7494b20e0`  
		Last Modified: Tue, 03 Jun 2025 13:31:36 GMT  
		Size: 296.3 KB (296292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab9a7a30deb311a783c5365d0931a1351ca72ae7fb5143ad20974e441e0182d`  
		Last Modified: Mon, 23 Jun 2025 17:36:02 GMT  
		Size: 80.5 MB (80523024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82341117b51eaec909e492783091ef149d1ae271a1f29e17d22d7213526aa3c`  
		Last Modified: Mon, 23 Jun 2025 17:35:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:6a01784a878b499815d02cd19e76a807bd37ec30f49bed17117f7be948337fcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae080253b9c17abd3a7b79b1cf744805d87e5129908a7680e22f47b2664d7044`

```dockerfile
```

-	Layers:
	-	`sha256:29b8759e6cb4ceca59ffb4b5933f14cf53bc6bc9d7a60f2bfbc56451aa4d76bc`  
		Last Modified: Mon, 23 Jun 2025 20:24:32 GMT  
		Size: 25.0 KB (25047 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v7

```console
$ docker pull golang@sha256:9574215fa12da44ad70aa23b550bfd3e082369aebaf6842ec45a0be6b76d13f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.8 MB (83791012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1462698fdfe233fd7c9a30e9e3974e5a3a45974a091616e7a86a04759c3237b7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 23 Jun 2025 05:23:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 23 Jun 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Jun 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6c9cae412d8d42471b3ec2789f87569712940a14bb5b06595436c95f2904f8`  
		Last Modified: Tue, 03 Jun 2025 13:31:36 GMT  
		Size: 295.2 KB (295232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2c23b36edc595b524e22ac037644488010f16b51c7c2741b5377b0b7319594`  
		Last Modified: Mon, 23 Jun 2025 17:37:09 GMT  
		Size: 80.3 MB (80276441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8b3081639b344da845748fe78e8a3f790c5472bd634b9b7428d029f2240ad5`  
		Last Modified: Mon, 23 Jun 2025 17:44:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:84ffc9e80d8198bd198bcd2de43e4c7f7c1064261d3e0a778fdb0487a773b0df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.4 KB (221353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ad2950722cfd06bf7c35e4f4524f8a535c8eacd5e9fc7e28c6a2fcf33e36e0d`

```dockerfile
```

-	Layers:
	-	`sha256:f2b14389238ecd6a679b5998f0c9eca88909099742eada5beb4e3ad808630517`  
		Last Modified: Mon, 23 Jun 2025 20:24:36 GMT  
		Size: 196.1 KB (196091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b26261a8c0625b2f78298233fffb726c24e7a46560f7d36f5f7f04283c088cd`  
		Last Modified: Mon, 23 Jun 2025 20:24:37 GMT  
		Size: 25.3 KB (25262 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:7443d59c7b881e5ae1d976eb6dff6112da756085f40b3f3783fd32bfbb19a661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83602408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a9f14775d3c7acc394fd78ff93767c4d85cb758a0bd4dbd1f37195775b9751`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 23 Jun 2025 05:23:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 23 Jun 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Jun 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8dd3ea6e04c1423d6090963e2686477f06c34a0dfdfd784acc48ae829d42ba6`  
		Last Modified: Fri, 13 Jun 2025 00:40:51 GMT  
		Size: 297.9 KB (297894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b77692401f3ea137343bd9363ea145d89603d5742a3fff804ed8b3a2b6ef06`  
		Last Modified: Mon, 23 Jun 2025 17:54:19 GMT  
		Size: 79.2 MB (79168414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21281cb34f1f0d990bed8bec5954b0399a44953c17a3511e1d5aada32c20aa61`  
		Last Modified: Mon, 23 Jun 2025 17:58:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:056f24fefac0d480ff3d1d68f47775fafef3f900b6ba949a8c99cb07fe7b1635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.4 KB (221423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873c139aab86279750bc7346171e3ce59505ecb3a05a74c083b136c3278303e9`

```dockerfile
```

-	Layers:
	-	`sha256:dad67b4bf71c795c9c1210354030a26c02591367d26cf764a34b102d0113e9ed`  
		Last Modified: Mon, 23 Jun 2025 20:24:41 GMT  
		Size: 196.1 KB (196125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c6ee8a9352d33a803dcaf64465cce4fe4cb37b63753186b943d9c7d58540e89`  
		Last Modified: Mon, 23 Jun 2025 20:24:41 GMT  
		Size: 25.3 KB (25298 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:63c937206f8571081d12bdf76875597ef5a8b102fbf9a8a03d3ac818aaa4f270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.8 MB (85840143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a04b79666b95465598a6b1b6e742fca62a5f7398d0c7d3e5eeb590154e7e64f3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 23 Jun 2025 05:23:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 23 Jun 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Jun 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce401225dbcfcefd49de03f63d418aaff77ccc05a109a46f584bd363b839daa`  
		Last Modified: Mon, 23 Jun 2025 17:36:21 GMT  
		Size: 295.6 KB (295616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361c3a68cf208e712d48fe5a3cca6178d38afd0dcfcac42ede03f6220d712b15`  
		Last Modified: Mon, 23 Jun 2025 17:36:27 GMT  
		Size: 81.9 MB (81928340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10bbfc7839c0e56df7b9cc2c830b58e4ef991186eef66170aedb7bff8487f34`  
		Last Modified: Mon, 23 Jun 2025 17:36:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:0fe2be774a21230bb618e7fefe79d00142b9f9ec1288e29662e9631b3b3afabc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 KB (221125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25bd591c3f603b5e08a62adbc884b819e3e2857ed31b28986d505dafbd1124bf`

```dockerfile
```

-	Layers:
	-	`sha256:115b2d04a48758cfb3620b5cc72d987f533c4a294f05e549e60da9d3bb502170`  
		Last Modified: Mon, 23 Jun 2025 20:24:44 GMT  
		Size: 196.0 KB (196030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e49d1511665b7495e8155815a0919d36fa5511e86d1d772efd4c20541b11394`  
		Last Modified: Mon, 23 Jun 2025 20:24:45 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; ppc64le

```console
$ docker pull golang@sha256:097ac0e28e7009cedf7e0b529f8f42f82fd4191af72bdbbeed1a513ed95e1178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84491820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b14463f4a42072f0733b5b0e25fbab7c2e70e0f934e06fa640933872dc1cfc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 23 Jun 2025 05:23:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 23 Jun 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Jun 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a187c79905be9977c8b81d03082bbff0333d20fe9ac9a7740864c66f7e0e5c7a`  
		Last Modified: Tue, 03 Jun 2025 13:31:43 GMT  
		Size: 298.3 KB (298320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51f6a9436457535ac561521e5803267cfa96280c8bee442d726995d270b958c`  
		Last Modified: Mon, 23 Jun 2025 17:51:06 GMT  
		Size: 80.5 MB (80463156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8a369f928c94c65d0daf4e8bfa03c771cdffd5b9583497cbe54abdd6e11824`  
		Last Modified: Mon, 23 Jun 2025 17:54:19 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:be6bef8c6ebe564c0c37be5532e155b4c3f497063af3957bb148017f7f550caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aac0c5d22cb6cdf68cddc209c6b31cbccba2b5614d062647e79e0333c776e7a`

```dockerfile
```

-	Layers:
	-	`sha256:2ca4cb16c96ea669292b3575ed1bb286a68d20801148421e024493ce9688bf39`  
		Last Modified: Mon, 23 Jun 2025 20:24:59 GMT  
		Size: 194.2 KB (194166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46597fa4f5cdf1612b289e87913f19999f01d06a0f3aa85b84ca88e95240d906`  
		Last Modified: Mon, 23 Jun 2025 20:24:59 GMT  
		Size: 25.2 KB (25196 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:6f0146fd333fca0c224630d18996272f7a2a6ccd07f249885940608e4f853ba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84471350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86decd014068694db24e51130c7d82fc7450c389c76518f9ae171b9cd79e3139`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 23 Jun 2025 05:23:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 23 Jun 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Jun 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850bf8006499bec04d28fe13dec3efd4cf9075748d5dcf5b6dc1415aa6aeb8f0`  
		Last Modified: Tue, 03 Jun 2025 13:31:45 GMT  
		Size: 295.4 KB (295390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca371f3980f40fcf4092a1b2596a15254585a582ae996faee1dffc84f633fec`  
		Last Modified: Mon, 23 Jun 2025 18:20:54 GMT  
		Size: 80.7 MB (80661991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c50291f899b816b81e3229a7073d8830ed84616512799307c4b5530c2021d5f`  
		Last Modified: Mon, 23 Jun 2025 18:20:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:722daebe0f3ccb0d7b3e0c084c91a4a9e7700a2f4ef6b90939dbcc9441a56836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f17812e7853a5ded9f366806d41dc46aea0e4e068f2b5689aa2a0d3ce60e3028`

```dockerfile
```

-	Layers:
	-	`sha256:0067cf7aef6f1223fe45edce2216186c3b41893b1c93955285f5817ca515e54f`  
		Last Modified: Mon, 23 Jun 2025 20:25:03 GMT  
		Size: 194.2 KB (194162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b49fdee754b3f55140c47f2535b14852de2e79227791ccb85439c87b3a72b2c9`  
		Last Modified: Mon, 23 Jun 2025 20:25:04 GMT  
		Size: 25.2 KB (25196 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; s390x

```console
$ docker pull golang@sha256:de9d9b88bdb570471ae3d6eee57edf5041a5cdf5ad145399f867d7ff0112117b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85652911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7264774ff7a8edbcd2da0827f9613b4babf07b5076c8aa4d65f888819e46513a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 23 Jun 2025 05:23:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Jun 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 23 Jun 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Jun 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Jun 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02725f6addf0718099c43b5965203aa513fc71aa710978afc18cf384dfb4798`  
		Last Modified: Tue, 03 Jun 2025 13:31:49 GMT  
		Size: 296.2 KB (296215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c4e9ad813ce53948d9016f3d50242da725640f347f8b2bb02b8db89e7d0980`  
		Last Modified: Mon, 23 Jun 2025 17:41:29 GMT  
		Size: 81.7 MB (81709009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce0ac803ce967e97487ffa1175e25dd38ca4417e7b1a2cd45a19f7bdda8c582`  
		Last Modified: Mon, 23 Jun 2025 17:44:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:d368c6ab1c02e7d6766f1756342806725830c6f4566311e1b8ee22e03a653e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.3 KB (219256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c99dcf8d7d417c2ed568e9fc8b352ad4bfa135631f5ee13a3988af62faed4e14`

```dockerfile
```

-	Layers:
	-	`sha256:7b6c353711e365c5125ec54dab13193243e522bc4b0824ce9d97da6d227616fb`  
		Last Modified: Mon, 23 Jun 2025 20:25:13 GMT  
		Size: 194.1 KB (194118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a5d264ade288d85905e1fc4025502fb99db7b8c936964541ce249f060fd47d`  
		Last Modified: Mon, 23 Jun 2025 20:25:14 GMT  
		Size: 25.1 KB (25138 bytes)  
		MIME: application/vnd.in-toto+json
