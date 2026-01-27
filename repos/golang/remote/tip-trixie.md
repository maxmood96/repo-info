## `golang:tip-trixie`

```console
$ docker pull golang@sha256:88ec7f14225b2b3e3a87d760201ea369181d5b585b61d252185fdc275653f534
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
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

### `golang:tip-trixie` - linux; amd64

```console
$ docker pull golang@sha256:2cc8d8ded4a9ebfbcc4419983e6e386b5b9c4e4df08d921c0fff0ca1bae15423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.2 MB (338179152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b598d58fb9ba579d11edf856e5e4d03e1b1e647a76f4687c60c5b91eff3c6c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 26 Jan 2026 22:05:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Jan 2026 22:07:29 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 Jan 2026 22:07:29 GMT
ENV GOPATH=/go
# Mon, 26 Jan 2026 22:07:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:07:29 GMT
COPY /target/ / # buildkit
# Mon, 26 Jan 2026 22:07:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 Jan 2026 22:07:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e18c5e1c15ff34b31f1443e9327b69daaa0c1bd65a23846328fc3738c7f8f1`  
		Last Modified: Tue, 13 Jan 2026 02:11:12 GMT  
		Size: 25.6 MB (25613410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be442a7e0d6f290b909f8da51840566e06ab51bfbea277c70fbda26c44c8259d`  
		Last Modified: Tue, 13 Jan 2026 03:54:29 GMT  
		Size: 67.8 MB (67786776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61bc0622e5bf2e3b34d5de9c35a7499508ce563901af4c3fb8d9a1d761a39290`  
		Last Modified: Mon, 26 Jan 2026 22:07:58 GMT  
		Size: 102.1 MB (102138649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606b852e3c333533b6267cbada59c6fbc954cef2b3af5c4c84f2f9bd6ca56999`  
		Last Modified: Mon, 26 Jan 2026 22:07:54 GMT  
		Size: 93.4 MB (93354538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9623b8210b9ae64eed15b77c64bc8943acd5b24580d02c4ba20e5471370752`  
		Last Modified: Mon, 26 Jan 2026 22:07:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:f099b460c4d9df5525ae24d692c2fef6ee5e3be313e3de1504a0f98854c24aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10814552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6b71327dd2660271d4d5175d2a8444602216b71fe4c3e1bc8aab6f2071bc53`

```dockerfile
```

-	Layers:
	-	`sha256:43cecedc4e8838f4cea84f5674c7986d15f8f245d91a324cad4d77a3ab99bc80`  
		Last Modified: Mon, 26 Jan 2026 22:07:55 GMT  
		Size: 10.8 MB (10785583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4747bf040f2ef8d60b1cbf571ff84fa5a11e26e990b8ed1cb1fe0b31d030bbc4`  
		Last Modified: Mon, 26 Jan 2026 22:07:54 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:f476f6d2bb0f5bc0fd6795751024c31cc646927007390b859965f122a2cdcafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.4 MB (294368331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371dc4c4b8e6476a307c72dc6757368b2f0c3b26a57f37e436adf8773d367b39`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:58:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:25:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 26 Jan 2026 22:11:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Jan 2026 22:13:51 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 Jan 2026 22:13:51 GMT
ENV GOPATH=/go
# Mon, 26 Jan 2026 22:13:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:13:51 GMT
COPY /target/ / # buildkit
# Mon, 26 Jan 2026 22:13:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 Jan 2026 22:13:54 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0f4296a8ece8abd5a409e5fbdb0cf93258815e4fec9dc768c39a63faf3c16052`  
		Last Modified: Tue, 13 Jan 2026 00:42:25 GMT  
		Size: 45.7 MB (45717820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8e700e2f18987ab9f97abcd0497d5dfc1706a8c057e685438ce3b71d8067c0`  
		Last Modified: Tue, 13 Jan 2026 02:59:04 GMT  
		Size: 23.6 MB (23626665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf6f5dfbcc297b2e354e856be84c591ec9f96e89fd8401a4d485596c43b8ed8`  
		Last Modified: Tue, 13 Jan 2026 04:26:01 GMT  
		Size: 62.7 MB (62713384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405dcaf6c63d3ea901c8088d1be0934da22b07549c0fa87f637d198b3e6c74d2`  
		Last Modified: Mon, 26 Jan 2026 22:14:20 GMT  
		Size: 72.8 MB (72783543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1205fc7a73de56b4f5ea25cad036ec0f33fb7b33229a77437a24f71a2e0db125`  
		Last Modified: Mon, 26 Jan 2026 22:14:20 GMT  
		Size: 89.5 MB (89526761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca90c8bab1238b06b0147c89436170772b8d634a0545b795bf62d0cf552320d7`  
		Last Modified: Mon, 26 Jan 2026 22:14:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:d3e7171c5922bec2f9e777c447505655f01ce6782e91948f7fc1776afc6edab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10610562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e116229779b8e0d1f9007be5af69afbe7c42e8c6a86c450ea14355d67df9fb49`

```dockerfile
```

-	Layers:
	-	`sha256:ff1ea862f1d06342ff2000ac0df6c6bd5e9f918bd4d32f428af640dbcecc6fcf`  
		Last Modified: Mon, 26 Jan 2026 22:14:18 GMT  
		Size: 10.6 MB (10581470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bfa3142ce30089613f0c85d3735a5561c573327b40c37046ca75188f1a7829d`  
		Last Modified: Mon, 26 Jan 2026 22:14:17 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:d6d313e687fcc8ed57ac1a842b7d649a9208f8ccb72e746efe40a0632e560a62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.0 MB (328963052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01fe80edae3648fe45ce3df96a6126f8fa1d59f670b3e24bf5436a5fbf1bec26`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:15:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:58:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 26 Jan 2026 22:05:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Jan 2026 22:07:37 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 Jan 2026 22:07:37 GMT
ENV GOPATH=/go
# Mon, 26 Jan 2026 22:07:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:07:37 GMT
COPY /target/ / # buildkit
# Mon, 26 Jan 2026 22:07:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 Jan 2026 22:07:40 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:42 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d5b6b6766fd729045e2e7d0396d1f61fe41c612d4aef6bb3bf5ea7db12ae2`  
		Last Modified: Tue, 13 Jan 2026 02:15:36 GMT  
		Size: 25.0 MB (25022636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b629762372f548de0ebccf01b8e80ae5ce251dfd36aef6fc3ae8d963493edf`  
		Last Modified: Tue, 13 Jan 2026 03:58:39 GMT  
		Size: 67.6 MB (67591513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b470fd086c86f57387b1a8f6249738e592767cb35df7b66866d072970cc9048`  
		Last Modified: Mon, 26 Jan 2026 22:08:07 GMT  
		Size: 98.3 MB (98283404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c3fde52f4a9ce3ba79f004ba1b1e261e66970dc6baaa4a0f9b9bee7c6d5ab5`  
		Last Modified: Mon, 26 Jan 2026 22:07:42 GMT  
		Size: 88.4 MB (88417257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d2e210c71543b8f34faa4c57c60bf1ccd7e60525889f2c8ec9ae00d4e37fd4`  
		Last Modified: Mon, 26 Jan 2026 22:08:04 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:e5dad89835b15ad8bd607906bec7ad1eee8b2a3f28a83733bda1d998d225ee47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10935162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25370ae3f643961635301272ec640d65e256b147dfcb61737323ddf970ac6f61`

```dockerfile
```

-	Layers:
	-	`sha256:f5b54950c0747e2f6e5f5d6a4058229ddae7674100c219b5a089312bb875aaaa`  
		Last Modified: Mon, 26 Jan 2026 22:08:05 GMT  
		Size: 10.9 MB (10906038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30d6c578b4cf442b7599ababfaa120f98f2d910dd57a21e8b9e654531ae2b6e8`  
		Last Modified: Mon, 26 Jan 2026 22:08:04 GMT  
		Size: 29.1 KB (29124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; 386

```console
$ docker pull golang@sha256:f292ff7b88adad3f3c554bde853b0f926a61ad8e037e5ecb1c1d69df652387d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.4 MB (339400989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28eefbb73e49b25cec4b0dd97bad2dca7611939cb11288a3956aa8f6190bdb1f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:03:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 26 Jan 2026 22:02:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Jan 2026 22:04:49 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 Jan 2026 22:04:49 GMT
ENV GOPATH=/go
# Mon, 26 Jan 2026 22:04:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:04:49 GMT
COPY /target/ / # buildkit
# Mon, 26 Jan 2026 22:04:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 Jan 2026 22:04:52 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1f0b243ad587d8f60f107748ba9fe54e338921c7b90e6a5d26e1d50d32f7481b`  
		Last Modified: Tue, 13 Jan 2026 00:43:28 GMT  
		Size: 50.8 MB (50798876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef949cdbd6ae265d5239bd005e65c3d578de54ebe10474ccd2feb9708b6e1843`  
		Last Modified: Tue, 13 Jan 2026 02:03:36 GMT  
		Size: 26.8 MB (26778274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ad78e3f6c783e58b723e0e1c78c005c2b612d1657c3a40830f5d7d97f9d85c`  
		Last Modified: Tue, 13 Jan 2026 03:04:46 GMT  
		Size: 69.8 MB (69803208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37278e9d59b119250d97b44f1dc7df3c02f2297ebbf888eb3568d1a413fd2355`  
		Last Modified: Mon, 26 Jan 2026 22:05:19 GMT  
		Size: 100.6 MB (100582746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb24967b184a59692854afa79a294d0d5b0fa84b707a952b78449312c20956e`  
		Last Modified: Mon, 26 Jan 2026 22:04:59 GMT  
		Size: 91.4 MB (91437726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992c407265163f1f29cd0d3c63d96d92ba07041477e27e5c4e76775fa48c48fd`  
		Last Modified: Mon, 26 Jan 2026 22:05:05 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:5bf114d91c3afe678a7ed0a3622881b2ebeb4de3895d8749991ac60c25a8269c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10785772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a802036db55db399e28abc0b0eebaf93142177b7f185351cc44e204fbb89340f`

```dockerfile
```

-	Layers:
	-	`sha256:00cde1a9e362cef085dc1fb9fe502d5f1a07319794458aabb11a0f8dc4fcde48`  
		Last Modified: Mon, 26 Jan 2026 22:05:17 GMT  
		Size: 10.8 MB (10756846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa8bea39719d0ca10020a7a3e4af4d70c0e1a7103ba1501be641ee3eb08777b9`  
		Last Modified: Mon, 26 Jan 2026 22:05:16 GMT  
		Size: 28.9 KB (28926 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:351159ba782a8882c59747d6ca41b32537eb69ef0102c022ed22e114b2b9eda9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (336038467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3aee473a514deb6eca3147f954adf30e5d0edc5b8eea8a7f81cd11d09392ad`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 09:15:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 15:18:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 26 Jan 2026 22:34:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Jan 2026 22:34:17 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 Jan 2026 22:34:17 GMT
ENV GOPATH=/go
# Mon, 26 Jan 2026 22:34:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:34:17 GMT
COPY /target/ / # buildkit
# Mon, 26 Jan 2026 22:34:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 Jan 2026 22:34:54 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:48 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21554c0ffe7aa9121703873815aca94dbbdf6352a46266dc923fc9e36d0d58a`  
		Last Modified: Tue, 13 Jan 2026 09:18:01 GMT  
		Size: 27.0 MB (26998052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb58d20828d54df35a08218c574236606c9e3ab14d0f2ddf036e12abcf8c85d6`  
		Last Modified: Tue, 13 Jan 2026 15:19:44 GMT  
		Size: 73.0 MB (73037608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f299da396ea322b76307435789793a9afff6d4f3627d0ee92fe1662c42c62394`  
		Last Modified: Mon, 26 Jan 2026 22:36:10 GMT  
		Size: 92.8 MB (92844762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db3fbdd047cc229947289d64050103b3f46ea0891f972e8e261f84917802eea`  
		Last Modified: Mon, 26 Jan 2026 22:36:06 GMT  
		Size: 90.1 MB (90050925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a0edd6fbabb1c425d3d34248a36a0fbe32f20bb1ab98a35c35c9e2548e4b42`  
		Last Modified: Mon, 26 Jan 2026 22:36:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:9abc2424688c90c650ef5212469ab56dc51303a5768d7368c61ab8788c895635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f42b11ec2c519390c9974f966408df4bcae307b089e21536e148ae59b041e94`

```dockerfile
```

-	Layers:
	-	`sha256:f44504992c9a0501592ba1c127548be59d51f7bda064182ebc7b38a42382a47c`  
		Last Modified: Mon, 26 Jan 2026 22:36:06 GMT  
		Size: 10.8 MB (10781371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c888b02c14423a4edae74fc1cfe39717ab7f2ca474d733f02b4ec466bd1064ee`  
		Last Modified: Mon, 26 Jan 2026 22:36:05 GMT  
		Size: 29.0 KB (29022 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; riscv64

```console
$ docker pull golang@sha256:b4de21036d28e6bab23281cd4d5aad3c7106e80c51c8acc4cde172ae5224da5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.6 MB (361596146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b359fdf83d01b34fbed1b3cbde3d1cd20e6c671efdd365cd60f8781c10ceb5d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 06:47:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 18 Jan 2026 22:58:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 19 Jan 2026 20:40:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 04:27:07 GMT
ENV GOTOOLCHAIN=local
# Tue, 27 Jan 2026 04:27:07 GMT
ENV GOPATH=/go
# Tue, 27 Jan 2026 04:27:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 04:27:07 GMT
COPY /target/ / # buildkit
# Tue, 27 Jan 2026 04:27:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 27 Jan 2026 04:27:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:559020494fc8527e77b291bee49cdac1db6bca66f8926cda195e0e4ebe7d2d3d`  
		Last Modified: Tue, 13 Jan 2026 01:06:14 GMT  
		Size: 47.8 MB (47770843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7f36a5fa281a3384abd9a90a26442f28edb507f1b9c537a07e1f5aaeb769a1`  
		Last Modified: Fri, 16 Jan 2026 06:49:07 GMT  
		Size: 25.0 MB (24952736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11f745939b2d13a20bc5767dafb02ca8b86a288cc70e3062fa70de76ce5b598`  
		Last Modified: Sun, 18 Jan 2026 23:01:52 GMT  
		Size: 66.7 MB (66660714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b6ae4171d4a5e53813caeec0fed4e819700c3a0b1ae7031301cbd179639a4c`  
		Last Modified: Mon, 19 Jan 2026 20:48:15 GMT  
		Size: 131.6 MB (131626895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336390632e3dab506cd0230c48180b8fdc0e8dcf2f397506712faf9caae798e8`  
		Last Modified: Tue, 27 Jan 2026 04:34:16 GMT  
		Size: 90.6 MB (90584800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42261ae4cff3c6fa073b72ddb5004ccfe23efff08f429f4515bb25e191a35b5`  
		Last Modified: Tue, 27 Jan 2026 04:34:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:5013b2e097b124c81d997859a394ea9443e651ab73c9a396a466d2e5cfed180b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10884230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609f361acfcf6491ac6c8c195096640970141ff8b6f6a7b8dd5622ba359a528d`

```dockerfile
```

-	Layers:
	-	`sha256:33fd5e1a1a416327d46550b53dcc1563f06aa1f5205135cc49d77d5ddb16ab9c`  
		Last Modified: Tue, 27 Jan 2026 04:34:04 GMT  
		Size: 10.9 MB (10855204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0696086416060372f780023f64cfe9409e21863c620942a3b989f3d7b5bc8bd`  
		Last Modified: Tue, 27 Jan 2026 04:34:01 GMT  
		Size: 29.0 KB (29026 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; s390x

```console
$ docker pull golang@sha256:9be9148c92a7d78ac715787befcc5ef345b9b69e3a1a170e1edbc1ff1a478410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.3 MB (313332072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760e9c4ce08d85f782cdcfc7c25b10b34372ddcce6a803fb580a421cbe2cf185`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:11:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:15:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 26 Jan 2026 22:09:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Jan 2026 22:12:13 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 Jan 2026 22:12:13 GMT
ENV GOPATH=/go
# Mon, 26 Jan 2026 22:12:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:12:13 GMT
COPY /target/ / # buildkit
# Mon, 26 Jan 2026 22:12:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 Jan 2026 22:12:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9de0288d81a9602539c9f3015fc521191e25eebfe6442c22cb974ea3a486f3a8`  
		Last Modified: Tue, 13 Jan 2026 00:41:46 GMT  
		Size: 49.3 MB (49348704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629a9411869af8d59bfb1073c3573138af1f96d808896b3f2fd14cf62fca6dba`  
		Last Modified: Tue, 13 Jan 2026 02:11:26 GMT  
		Size: 26.8 MB (26792892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff54b33211ee85001fc045dcc86b026876894b17d1d6f873a415014f68cb0c9f`  
		Last Modified: Tue, 13 Jan 2026 03:16:06 GMT  
		Size: 68.6 MB (68632678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e66565829b022f1348a6db2577b95f109a914963207602689c86969160a86bd`  
		Last Modified: Mon, 26 Jan 2026 22:12:54 GMT  
		Size: 75.9 MB (75949621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d1ebc1a42fde765fe01b70de439084ec52a344bfa25acb00b6d281dc10102e`  
		Last Modified: Mon, 26 Jan 2026 22:12:55 GMT  
		Size: 92.6 MB (92608018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1426ab94b36ffef81986d1cd3e45066337d5c115e302c97f8b89f0bdcb78b3e`  
		Last Modified: Mon, 26 Jan 2026 22:12:53 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:06d8048aebace5b2b59f27690776452f0a358cee375f6882db3fe29e457879b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10624947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b131df5b7b51e580ecda4b6d4b3dbc4670b2ea9aaa48938db07c845b28c675f`

```dockerfile
```

-	Layers:
	-	`sha256:80afe9564a7188827e194cf7e5da21f5ab7c6a24e29410f8322da06a6f53f928`  
		Last Modified: Mon, 26 Jan 2026 22:12:53 GMT  
		Size: 10.6 MB (10595983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de9c51c12e8486d80bffbe9d568028e1a6344923c620c93d2d5fc760d83a6696`  
		Last Modified: Mon, 26 Jan 2026 22:12:53 GMT  
		Size: 29.0 KB (28964 bytes)  
		MIME: application/vnd.in-toto+json
