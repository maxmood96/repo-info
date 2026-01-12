## `golang:tip-20260109-alpine`

```console
$ docker pull golang@sha256:d0c68397274169000371147ade1f26e74866b79eff5851ed6704424b7a3f82d8
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

### `golang:tip-20260109-alpine` - linux; amd64

```console
$ docker pull golang@sha256:ca5302b95d4cb1cc2e7b41eb31b9616298828c3def5fa73c9d3e6e69d0a5dae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99208195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:116c0cb58282709863a208d82ccd3841b3f280bac14e144c2e87752600a54d64`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 12 Jan 2026 20:03:16 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 12 Jan 2026 20:04:55 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 Jan 2026 20:04:55 GMT
ENV GOPATH=/go
# Mon, 12 Jan 2026 20:04:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:04:55 GMT
COPY /target/ / # buildkit
# Mon, 12 Jan 2026 20:04:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 Jan 2026 20:04:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3741072473740b6c71a53cb0ee9cc888c98b921cfe1495afd1bcff46084daaa`  
		Last Modified: Mon, 12 Jan 2026 20:05:17 GMT  
		Size: 296.1 KB (296084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e09070cc4c8c6b4577469e540a043174ece319f2134af5f8b6f76f4d7806aa`  
		Last Modified: Mon, 12 Jan 2026 20:05:02 GMT  
		Size: 95.1 MB (95051851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728152f413927e4813578519882c46e982cdd6309ba8acaf4a4e8c770625e40d`  
		Last Modified: Mon, 12 Jan 2026 20:05:17 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260109-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:54820135d6d8e92d30466ae25066b0b8fded8dfef64ae1beab954c0a555b834f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 KB (220696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f35db491814b3a8cda07617b40fd433aef2215dc3476f9543ccef082d21a607f`

```dockerfile
```

-	Layers:
	-	`sha256:ec0d95dbcee1b5f206e89f9c77dd71b773daa92b87ce3228abdce1e3e4118744`  
		Last Modified: Mon, 12 Jan 2026 21:24:18 GMT  
		Size: 195.6 KB (195601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db5a0095bc8878c6be71a659ae2592f82bf24a0a3e1db0612e69627e5e7d5b60`  
		Last Modified: Mon, 12 Jan 2026 21:24:19 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260109-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:0bc14cfcd9b2aba4cc69c0d732004b30cc13e6ad4b85a70ba27b77cd3e60dc6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95266864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffacdf8debf05238892ac9628fdc1cf4d68782a1d3b6400cad3e4508535287c7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 12 Jan 2026 20:05:04 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 12 Jan 2026 20:07:42 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 Jan 2026 20:07:42 GMT
ENV GOPATH=/go
# Mon, 12 Jan 2026 20:07:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:07:42 GMT
COPY /target/ / # buildkit
# Mon, 12 Jan 2026 20:07:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 Jan 2026 20:07:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f72b351a338f4bb050b91c885dcbfbbf9cddb7128898e7a6a7874181d48bb14`  
		Last Modified: Mon, 12 Jan 2026 20:08:06 GMT  
		Size: 297.3 KB (297267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fafe2d1996fb8d6337cd2dcb6acca5b8c22581c5ef4fda1f58bec46f2b5c18f`  
		Last Modified: Mon, 12 Jan 2026 20:08:13 GMT  
		Size: 91.4 MB (91401008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81db41473b5ca1a1008dbe0b46a08e1045fca7b8f4dd8112d4d8a0c6478cfef`  
		Last Modified: Mon, 12 Jan 2026 20:08:06 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260109-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:890711e735369af95e32e212fb747bd5c040960063cf7d53c4ebd88fbc4767e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f2c82ea4b914cd180725252089d03caba35009c0192b2b85e809bced223c332`

```dockerfile
```

-	Layers:
	-	`sha256:99b447491d1cad4826f023f4b01160838940d428225e2da7eb6929b7304dbe0c`  
		Last Modified: Mon, 12 Jan 2026 21:24:23 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260109-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:dcc720cb2c2d0406b2e39c2013a49ab417231dc1f313577a60957d83d60a54b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94710145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56fa502a68740ab8f1333ec2c1765ebe4937a668f58424d3d203a882b8838c1c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Mon, 12 Jan 2026 20:05:17 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 12 Jan 2026 20:07:56 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 Jan 2026 20:07:56 GMT
ENV GOPATH=/go
# Mon, 12 Jan 2026 20:07:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:07:56 GMT
COPY /target/ / # buildkit
# Mon, 12 Jan 2026 20:07:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 Jan 2026 20:07:59 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c343e5bb70e49d363be6805c730fdd3e8c6137e1d91a35996ab5d922485d01b0`  
		Last Modified: Mon, 12 Jan 2026 20:08:20 GMT  
		Size: 296.2 KB (296205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb06c5933c094de46d52df9ed5d5962ecacceb10cdc72056e1307b0ee8c18640`  
		Last Modified: Mon, 12 Jan 2026 20:04:47 GMT  
		Size: 91.1 MB (91134394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6a8419fef6c3c0326e8d053afbf3d0fc98c785c0a8e5d9137d6f7dd311a9d0`  
		Last Modified: Mon, 12 Jan 2026 20:08:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260109-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:1f71228d62986048216f76ae78935ecd53f096b630d96daa8591327b00adae32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd3c39143fefcbf51f65039c2932a6e8fb7110c715822c73e2b35f62b96df63`

```dockerfile
```

-	Layers:
	-	`sha256:3429a0f28458236dedbf5dcdcfc861999857b8747d823c43914eca68e75f68d2`  
		Last Modified: Mon, 12 Jan 2026 21:24:27 GMT  
		Size: 195.0 KB (194971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8fdde5a26311fee756bc890b79ac284b03da7d42ddbe7f64a54ff9fa75c6108`  
		Last Modified: Mon, 12 Jan 2026 21:24:27 GMT  
		Size: 25.2 KB (25222 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260109-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:5930b218bc7e7ddcf246a57a8914b147c94bdf7864d250bc66eddf84671c2d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94632052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b738f4dcffdbb40e66a90adee5d2aabc67e476bf947282ca30a1aa442db9611`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 12 Jan 2026 20:02:04 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 12 Jan 2026 20:03:43 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 Jan 2026 20:03:43 GMT
ENV GOPATH=/go
# Mon, 12 Jan 2026 20:03:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:03:43 GMT
COPY /target/ / # buildkit
# Mon, 12 Jan 2026 20:03:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 Jan 2026 20:03:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45de9669b6933f4d0d8f773656d1de4c295f543ab40c1919b622e8904442bfe`  
		Last Modified: Mon, 12 Jan 2026 20:04:19 GMT  
		Size: 298.8 KB (298846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cab7771dc3fd9d6c93b2e8fcd20d3b05cdc987b52c3e09c78b1417acc8931f2`  
		Last Modified: Mon, 12 Jan 2026 20:04:26 GMT  
		Size: 90.1 MB (90137309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f27f61ca3fa949fdbead221de98fe43e02b96aefad911c3116277e8925cfc7`  
		Last Modified: Mon, 12 Jan 2026 20:04:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260109-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:ab950fc891fa3b7a0f438e33056f7524f61bc26cfff66204538d315f2b0d2cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.3 KB (220262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39aff4f6527c67f262fda803d2f14677a7c3e20a21c17df58a153eb7c69db86e`

```dockerfile
```

-	Layers:
	-	`sha256:616c0923a5bbcac369f574a300efdfc9911965c690984dbf3a701cc505a380de`  
		Last Modified: Mon, 12 Jan 2026 21:24:31 GMT  
		Size: 195.0 KB (195007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe80cc84c2a2d3108c886a97ebc7bb73923f6fdda58720d80dd0c0eade6e87ba`  
		Last Modified: Mon, 12 Jan 2026 21:24:32 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260109-alpine` - linux; 386

```console
$ docker pull golang@sha256:1fd87e2faaab788c9bee732276d9fc2a4e480afc464deddb2ef6c1bcd358044d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96928485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7637535293cc8d1436df82c36cc89c0e744047d44b4cde9a119cb56354475a3b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Mon, 12 Jan 2026 20:03:35 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 12 Jan 2026 20:05:38 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 Jan 2026 20:05:38 GMT
ENV GOPATH=/go
# Mon, 12 Jan 2026 20:05:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:05:38 GMT
COPY /target/ / # buildkit
# Mon, 12 Jan 2026 20:05:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 Jan 2026 20:05:40 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfaa1a70ceda84fe1858819064f69911d12afa2c28aa21d536d2fcd98c336ef6`  
		Last Modified: Mon, 12 Jan 2026 20:06:00 GMT  
		Size: 296.7 KB (296673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42b2997976651e9da981a359adb745663b505ba580ded35d1fcd67a84ec5f37`  
		Last Modified: Mon, 12 Jan 2026 20:05:45 GMT  
		Size: 92.9 MB (92945554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5e971a11e8c078edcf14e295a61045ac98b5c27576ff636ecd24b0d3984206`  
		Last Modified: Mon, 12 Jan 2026 20:06:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260109-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:2cd6e939be8173aa42b5e834f6c43a014dfe0f99d086148356c8f30070c2ab02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355a3d42e430a51612a9e268aabf790d3ac912bf6d01ead9b80bba0c86542990`

```dockerfile
```

-	Layers:
	-	`sha256:91997ce0fdd3487cf9be7cb6cd8f65884dc767b00e02056959360f944b8dd06a`  
		Last Modified: Mon, 12 Jan 2026 21:24:36 GMT  
		Size: 195.6 KB (195560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f5790afa6c93cfb4486ed2b289c2982ca4215a2876fe18aa9c1ea29b4af7aa1`  
		Last Modified: Mon, 12 Jan 2026 21:24:37 GMT  
		Size: 25.1 KB (25052 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260109-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:6a97a5156449fe2e0ed165c3523bf7f3f604055af5f64556676c065ce8ce1595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95811090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd59df19f6559fc1b981ad125bb7c237f1065c58316f2331b58598f9f60163be`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:36:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 12 Jan 2026 20:05:00 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 Jan 2026 20:05:00 GMT
ENV GOPATH=/go
# Mon, 12 Jan 2026 20:05:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:05:00 GMT
COPY /target/ / # buildkit
# Mon, 12 Jan 2026 20:10:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 Jan 2026 20:10:33 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c251744709998ea3415429d77aa83c1ba367b71bf12c4b11c84d3ff1d0c4b550`  
		Last Modified: Thu, 18 Dec 2025 01:37:40 GMT  
		Size: 299.3 KB (299257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c1f34a163f68379a85adaf1396976b01cd79b6100ad42ff3e6581c97310f7b`  
		Last Modified: Mon, 12 Jan 2026 20:06:42 GMT  
		Size: 91.7 MB (91683920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1dc7fdeddbaac1a18b568f71a7847bb7067feda3247320c97cd2282859df42e`  
		Last Modified: Mon, 12 Jan 2026 20:11:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260109-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:0e6d33723563d3ab4e47a9a583ddeb9de584d8ec5416fdd244be71d2750d9789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:660e0d5da687c0b4bb3986e612e28820116eaa1ef97dd1721c025fd616e67667`

```dockerfile
```

-	Layers:
	-	`sha256:0a96caaaa1eb6674961cfdeac4970cd7979d83ac182918179c549adb3ad582c3`  
		Last Modified: Mon, 12 Jan 2026 21:24:40 GMT  
		Size: 195.0 KB (195000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:327290aa83c3cf62e7e52479d8029c620ebd82762c3489538771fb19f673d714`  
		Last Modified: Mon, 12 Jan 2026 21:24:41 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260109-alpine` - linux; s390x

```console
$ docker pull golang@sha256:134852ff8119d0ad0b73bc39329c1d9c4d3a93ac2d5c4abe1594b6ef528078d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.3 MB (98251565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2d117df38fb0a876b1ef23e0073dcb75d98c4407c5d5c76377aaab93e28917`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:14:25 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 12 Jan 2026 20:19:09 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 Jan 2026 20:19:09 GMT
ENV GOPATH=/go
# Mon, 12 Jan 2026 20:19:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:19:09 GMT
COPY /target/ / # buildkit
# Mon, 12 Jan 2026 20:19:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 Jan 2026 20:19:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7224d7d29671ca737c9ec945a7373478caed2bbfb74b122f8685b8c92149198`  
		Last Modified: Thu, 18 Dec 2025 01:15:01 GMT  
		Size: 297.2 KB (297192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560c721b150b3efd4976a8fc9ccaf826512a0d88981fdddc7ad84ff81c3bfa69`  
		Last Modified: Mon, 12 Jan 2026 20:21:03 GMT  
		Size: 94.2 MB (94229904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1cebdc0fa38665fa8816b0bb020292cf3041873bf42215a3faa2051a1c5b43`  
		Last Modified: Mon, 12 Jan 2026 20:20:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260109-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:413d5a6a14cb0c58de177f903c268f9b451eb877be55bcb6e621e7fc7b8a4550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 KB (220045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5471468bca1b761379572a8bd538d5de21264c37098677c76d6e2d3259466666`

```dockerfile
```

-	Layers:
	-	`sha256:1ebc685e26d43535ef8c00bba8583921db231c2e049d72a6b91b003f8bd748cf`  
		Last Modified: Mon, 12 Jan 2026 21:24:45 GMT  
		Size: 194.9 KB (194950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bd14b37027fe97cf9157f4ee6698762d3a74d9d0c3b0defb6dbaf4b9b1ae97c`  
		Last Modified: Mon, 12 Jan 2026 21:24:46 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json
