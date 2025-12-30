## `golang:tip-alpine3.22`

```console
$ docker pull golang@sha256:8f91efbc79edf461c023fad8bfb968359bc7f79d7c7c4f6d1b7465ac94c2abd8
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
$ docker pull golang@sha256:a643012c592e73748c1374b0baaac988575f3c29fa8f7760689cd0b7fa87dd40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99138379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d447cd12307aff3bbeb13e4b6dac7e487c7b6cfd45b51cd6161ded781a2b713`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:14:42 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 29 Dec 2025 22:16:36 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Dec 2025 22:16:36 GMT
ENV GOPATH=/go
# Mon, 29 Dec 2025 22:16:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 22:16:36 GMT
COPY /target/ / # buildkit
# Mon, 29 Dec 2025 22:16:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Dec 2025 22:16:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2b6e5b88dd05b3b1c1146cb59282a1bb66ccfa6ffe4f121988d7d97db09e9f`  
		Last Modified: Mon, 29 Dec 2025 22:17:00 GMT  
		Size: 291.2 KB (291156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7c54e75f0355977f49fd303fcd47e9c421e5cb4ce0639b9b1710d2f526d135`  
		Last Modified: Mon, 29 Dec 2025 22:17:03 GMT  
		Size: 95.0 MB (95044613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b711cf556b90c29b0565d8ce784614bc0a55b2a9a43da7eae244b5f3ea848f`  
		Last Modified: Mon, 29 Dec 2025 22:17:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:a86cbba5e84fef639ca11ef5b78ba34e19f3ed42313aae872a3d121399ad52c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9b222eb95b376443e68937fa9149d591ff29ca5610ac6e1cac09848c2b916b`

```dockerfile
```

-	Layers:
	-	`sha256:9602b9744858f27b932b917a3424891b574d8e9a11f5fc53139fd03ff28f4782`  
		Last Modified: Tue, 30 Dec 2025 00:26:15 GMT  
		Size: 195.0 KB (194982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f637d7036f19f0121434c1cc512f1d01e77154d0f24b7b13605b73612239c354`  
		Last Modified: Tue, 30 Dec 2025 00:26:15 GMT  
		Size: 24.5 KB (24464 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v6

```console
$ docker pull golang@sha256:0726c9bdf16e0fea850b1bfda9ca2b85877d7c646e245fb8903fa020c470a0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95191003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10b12622d779e113944f7ceb5c930d5a6fb2b308a6f58a5c4f98fed35a2e6269`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:16:12 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 29 Dec 2025 22:18:52 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Dec 2025 22:18:52 GMT
ENV GOPATH=/go
# Mon, 29 Dec 2025 22:18:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 22:18:52 GMT
COPY /target/ / # buildkit
# Mon, 29 Dec 2025 22:18:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Dec 2025 22:18:55 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Sun, 07 Dec 2025 22:05:32 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b25dd2072ec27d3909acc72cabeaf9ae92c9a14b3a5177c5360aecd0be629c`  
		Last Modified: Mon, 29 Dec 2025 22:19:13 GMT  
		Size: 292.3 KB (292325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f655f252e9ea0da9647bd4425fda60ae8c3fdfd44e08b5203fb635166f3abd4`  
		Last Modified: Mon, 29 Dec 2025 22:18:35 GMT  
		Size: 91.4 MB (91394440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2535565f3f75794f5e94900ec956fbdda7aea742502ac037524a5fa335c6ae2`  
		Last Modified: Mon, 29 Dec 2025 22:19:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:989ca76f21f65b8d5c4fa96f52c2c9223addb0e4c2a69677fc7fa6e7151ca91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e50fb2f0d392ed955ca24aa1b609e3f3621a48475a82572b057e66bffea43c6`

```dockerfile
```

-	Layers:
	-	`sha256:f7b1c1ded5d60d12111bc9c9830cc27e355fc645de8ab114b8548728d1cb5c0b`  
		Last Modified: Tue, 30 Dec 2025 00:26:18 GMT  
		Size: 24.4 KB (24362 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v7

```console
$ docker pull golang@sha256:7cbdca07e82f79146439029b3efb248dec8d468da8acf33f82fddb78ed7a0c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94627458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfcf2a6ff40a8f5831b6767e7bee100dabc7d311c35d271ee0c4d3aa2022423a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:15:03 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 29 Dec 2025 22:17:39 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Dec 2025 22:17:39 GMT
ENV GOPATH=/go
# Mon, 29 Dec 2025 22:17:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 22:17:39 GMT
COPY /target/ / # buildkit
# Mon, 29 Dec 2025 22:17:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Dec 2025 22:17:41 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Sun, 07 Dec 2025 13:57:17 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea657f851e6b551579dc7381412c55422c4b3e96057e4c7da2ac0f3b821d5523`  
		Last Modified: Mon, 29 Dec 2025 22:18:02 GMT  
		Size: 291.2 KB (291212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a592f218adec4eba0bdf6f4ba76e47643fbd079be331ecdb85fd7600664dc026`  
		Last Modified: Mon, 29 Dec 2025 22:16:40 GMT  
		Size: 91.1 MB (91114533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71556982010f22c8d79a1b829984b04a38931d86b0d9b13e5f02c189903e9ce3`  
		Last Modified: Mon, 29 Dec 2025 22:18:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:768dd12afd9f291b0e57846e4f4e81b00a9aeebfc7c5c574de62c81da5d60fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 KB (219563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a051dd7b35942ae191c76e5c973c9c07662d0bcf1b3bb61a9fca937aa562014a`

```dockerfile
```

-	Layers:
	-	`sha256:4f1dbbbc44029da3deb4e428ed54c7283c4d9704c48648ca62f2c65ce54ae1f4`  
		Last Modified: Tue, 30 Dec 2025 00:26:21 GMT  
		Size: 195.0 KB (194986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1a4adff08f56e3d5e3a24e20b5f7fddc365c41a2209623d186f1aac530b654c`  
		Last Modified: Tue, 30 Dec 2025 00:26:22 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:8ee6f7718d09256580513b2fb11e4190318ac444cd7622d3b5d3308043cbb044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94557310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:797b0f63fb7aa6b0cff2eb566e25af4013ecc5c0c098ceba7cee98713927c08d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:14:40 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 29 Dec 2025 22:16:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Dec 2025 22:16:19 GMT
ENV GOPATH=/go
# Mon, 29 Dec 2025 22:16:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 22:16:19 GMT
COPY /target/ / # buildkit
# Mon, 29 Dec 2025 22:16:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Dec 2025 22:16:22 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb6c60a0844f6e171fc4a99faaea2bd3df14052d42fa003c47570575c81038d`  
		Last Modified: Mon, 29 Dec 2025 22:16:43 GMT  
		Size: 294.1 KB (294100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ff2a18ac08f0eac3e3d9e16d67bcab1f49cd95a40840a22cede89724436815`  
		Last Modified: Mon, 29 Dec 2025 22:16:45 GMT  
		Size: 90.1 MB (90124983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:456270cc2e635e33ad06a427c9a4068df03fd3b87876a588cece882db4d3332b`  
		Last Modified: Mon, 29 Dec 2025 22:16:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:5040bcfb8736b147b022ce24dab5e5847d26e272df6aa6e2b10946ddd725e7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 KB (219615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8682d68540b9629a10d72b15f39d6fa26f4e5eb9ec8fe07d26b4d56acb785516`

```dockerfile
```

-	Layers:
	-	`sha256:fd9f99fd971e84db7b135974ac1821f036bab5acecfabcb008b35b0b5be055c5`  
		Last Modified: Tue, 30 Dec 2025 00:26:25 GMT  
		Size: 195.0 KB (195014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddf0ea2be290b965c3b73c03034e8269a36d612381d7fd052d306d7cf2aa97a9`  
		Last Modified: Tue, 30 Dec 2025 00:26:26 GMT  
		Size: 24.6 KB (24601 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:6939413291129dfa4522f6d2a071f9dcb1e5c315d5f94ab4e1041a889e305a65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.8 MB (96849429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54fc3784f11c168e94843f2e1b7494a66a1d737e6db8342fe25e5fd450131c9a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 29 Dec 2025 22:17:28 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 29 Dec 2025 22:16:49 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Dec 2025 22:16:49 GMT
ENV GOPATH=/go
# Mon, 29 Dec 2025 22:16:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 22:16:49 GMT
COPY /target/ / # buildkit
# Mon, 29 Dec 2025 22:19:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Dec 2025 22:19:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Sun, 07 Dec 2025 14:06:47 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9267bf8860a64d8258c0db6e1e98ca1ad27041842e363b8bb157ff390b762a79`  
		Last Modified: Mon, 29 Dec 2025 22:19:36 GMT  
		Size: 291.6 KB (291635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b6f0074455116012c1ba771d20edb2ec10d2462257d60366f8ccb9b9224a99`  
		Last Modified: Mon, 29 Dec 2025 22:17:35 GMT  
		Size: 92.9 MB (92938705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e57dcf2251850d5a1b53d10531eb3dbeeaf79a96ed1a53926e59e864174c0d0`  
		Last Modified: Mon, 29 Dec 2025 22:19:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:6cb52275a02525779db29dd10d1c2eba79ebb086f87431938028d78be1db0db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6819ffb5af0c435a363644a1570ea3c047afc4c613f3f390a58f0f45a5f872c0`

```dockerfile
```

-	Layers:
	-	`sha256:90253d082c42bbe2f688fc01565c1a3d2e912c9f27f3a1659986997b19a776fa`  
		Last Modified: Tue, 30 Dec 2025 00:26:29 GMT  
		Size: 195.0 KB (194951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d358b61d8547420ebb8e33d874b2ef420f332837a470a6986787d491095c436b`  
		Last Modified: Tue, 30 Dec 2025 00:26:30 GMT  
		Size: 24.4 KB (24432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; ppc64le

```console
$ docker pull golang@sha256:7f8109ca18af8c47e8866f0a54cdff367154664a338621078123ddf8af7e23f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.7 MB (95684994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c45304a31ed3f4c67cd3ebbb17d0fb11400992d65b27c3038d9c81d2acccff55`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 24 Nov 2025 22:43:33 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 29 Dec 2025 22:16:29 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Dec 2025 22:16:29 GMT
ENV GOPATH=/go
# Mon, 29 Dec 2025 22:16:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 22:16:29 GMT
COPY /target/ / # buildkit
# Mon, 29 Dec 2025 22:21:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Dec 2025 22:21:08 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Sun, 07 Dec 2025 14:06:45 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64958bce21ae47528776dd8bd6794140e1f5086c72ae8807ba8f48bb37fce769`  
		Last Modified: Mon, 24 Nov 2025 22:43:59 GMT  
		Size: 294.6 KB (294592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d98e6a9db6f27c232427cc65a14243d3dc0a9f5145a0455e78bccfb2bf7249c`  
		Last Modified: Mon, 29 Dec 2025 22:17:47 GMT  
		Size: 91.7 MB (91658002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c4f973c3ac85deb2b6c068b00076cf81b9e886ccac585fde54f544b11e188c`  
		Last Modified: Mon, 29 Dec 2025 22:21:34 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:3569919d7ed3d930c1760a4af31ca902ad200745da8b1e471dc2a3c21e83ef83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 KB (217580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b5482518fcdfd17bcd5201cc6b4cfe705467d2cb11c431645ab8e97ac99a71`

```dockerfile
```

-	Layers:
	-	`sha256:ccb5bd439dbd99236949e38c1d7fbabefd85313e64493484321fff2b696285fc`  
		Last Modified: Tue, 30 Dec 2025 00:26:33 GMT  
		Size: 193.1 KB (193069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a2e2824de65c1e73553d8eb7923ae2f546636aa4c08a8d8e31263df40b3fa06`  
		Last Modified: Tue, 30 Dec 2025 00:26:33 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:e9ce4b9105eae66b1975b79089387f6b3b4370302b6b018ec46591419318a193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96114451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df19799c3a48a1c0faae4bc4bfb594a08d04055c18b648b54f62f04c58114065`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 25 Nov 2025 07:20:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 29 Dec 2025 22:59:48 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Dec 2025 22:59:48 GMT
ENV GOPATH=/go
# Mon, 29 Dec 2025 22:59:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 22:59:48 GMT
COPY /target/ / # buildkit
# Tue, 30 Dec 2025 00:22:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Dec 2025 00:22:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Sun, 07 Dec 2025 22:49:04 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a984176d166c6f9d398140e2c603deed3f1a52311d2a418b830c1cfdaffb3c`  
		Last Modified: Tue, 25 Nov 2025 07:22:38 GMT  
		Size: 291.5 KB (291523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b4b43eddab816a91e4e75ac1e1a8a3a105423311aff668e1c7594d9f8bed52`  
		Last Modified: Mon, 29 Dec 2025 23:07:05 GMT  
		Size: 92.3 MB (92307532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4714d40883cb8e1c41f52c85a74395130649747ec9cbc6783f1a74c9041341d3`  
		Last Modified: Tue, 30 Dec 2025 00:23:50 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:1bb4ab1fec4167165d05734b69bde879ba4ae31032a18cefd15d70361488117f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 KB (217576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bbad3314f7fc0ce62be99516e095e7c227229938ce1206dee2629854df02e84`

```dockerfile
```

-	Layers:
	-	`sha256:fe111efb11d4e3b32de619f2b5d080c168afde0c7af81d287820314e5dac8def`  
		Last Modified: Tue, 30 Dec 2025 03:26:19 GMT  
		Size: 193.1 KB (193065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e243a6f66bccd018d75ddead5e4bab134980b4a71a17114caaab420204505aec`  
		Last Modified: Tue, 30 Dec 2025 03:26:20 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; s390x

```console
$ docker pull golang@sha256:9cb50dd99a99fb49e13540bf3fe7dcb7aa96c3a1ecf9b430a8eb241abe32fe2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98145410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e76e35c054bcb8e28655169541637c13adf67d59289f14b5b856dbd9382505`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 00:42:03 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 29 Dec 2025 22:16:41 GMT
ENV GOTOOLCHAIN=local
# Mon, 29 Dec 2025 22:16:41 GMT
ENV GOPATH=/go
# Mon, 29 Dec 2025 22:16:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 22:16:41 GMT
COPY /target/ / # buildkit
# Mon, 29 Dec 2025 22:16:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 29 Dec 2025 22:16:43 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Sun, 07 Dec 2025 14:06:46 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2a05f09601b30b4f54a2a9acd5043671541b70f912b9dea60733fd4213fbc8`  
		Last Modified: Wed, 17 Dec 2025 00:42:32 GMT  
		Size: 292.2 KB (292152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25ce8a7fa174e9abbfa1259cfd0fba44c900e27f7f4a5ae1c83f6fe0801a275`  
		Last Modified: Mon, 29 Dec 2025 22:17:17 GMT  
		Size: 94.2 MB (94203858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aed745b64ad253a3a1681403c7cd482bc2713908084e23ab15f3d30c4e95d6b`  
		Last Modified: Mon, 29 Dec 2025 22:17:10 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:7ea3deddca20b23809238a2aafa3f8abc84ad6881f863c93906754b7db120620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 KB (217496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28248f233c35fb656b66be98b4dfad5938e3cf026fdfa442230fa43c8c93c306`

```dockerfile
```

-	Layers:
	-	`sha256:fd2399231019f356a6c8a991b567206feb1174d2ca65b65501312a9aa1389670`  
		Last Modified: Tue, 30 Dec 2025 00:26:36 GMT  
		Size: 193.0 KB (193031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f20b17483207b526db9b1b8d120e14518e58c92d9f54569af00169344a770ef`  
		Last Modified: Tue, 30 Dec 2025 00:26:37 GMT  
		Size: 24.5 KB (24465 bytes)  
		MIME: application/vnd.in-toto+json
