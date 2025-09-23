## `clojure:temurin-11-trixie-slim`

```console
$ docker pull clojure@sha256:5b60fa8750f1e5e49a5fa044709668f4bd882918ad12038fda7ac06ca871429e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f87172b125169cd1857ef43ca90a7ec3fa790cd64e4957a5d285530dd6842614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 MB (247418562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c2af232c98afbb93b96118f36f920efac2e4dc3eab6034aca416651f009cbc`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd808b6713d16a6d07e9f7b19eec55fe7f9e256359de4e7c3c816fb94634785`  
		Last Modified: Mon, 22 Sep 2025 23:45:11 GMT  
		Size: 145.7 MB (145658257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ef7c623d8ff6c8f2937e9379ba0041b6f429fcc987bbf0208df2ffe4be24c8`  
		Last Modified: Mon, 22 Sep 2025 23:45:35 GMT  
		Size: 72.0 MB (71986165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11921a50ac862d98dc0bb58c2855ecbee732b324d05e0865f482e3f827c5e604`  
		Last Modified: Mon, 22 Sep 2025 23:45:28 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:db6dbfabbc59c9cfde7442a22636b2059da1842760429b2d96cb6e8eb6c4a314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5290540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b29b24eb7abe62005a7ff7c3796af30bba2fb626f613d67c9781be9c81b1f1cf`

```dockerfile
```

-	Layers:
	-	`sha256:f7e71ce3977ff4b271178bcaaead40f5093ffc53e522b7e4b6dc1343df963427`  
		Last Modified: Tue, 23 Sep 2025 00:36:57 GMT  
		Size: 5.3 MB (5276254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8d72f84fb1b3276d431a46bc66c18a8e27241c75c7c7a0da274f6f057c6c460`  
		Last Modified: Tue, 23 Sep 2025 00:36:58 GMT  
		Size: 14.3 KB (14286 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e3ecd6e891ce2cc90f0d8c5a88a25dbeccd9a1f2fa45f8b4bd87dcdbd841ea70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.4 MB (244400764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cabae6a813ec9fd0174fe558d46707b432eb83b72c4300e7257929848f2814b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6e7c437f2607fb7f3b8e2e0800b767b6b9535c8feaa3913dc9a0a864f3723a`  
		Last Modified: Tue, 23 Sep 2025 20:29:04 GMT  
		Size: 142.5 MB (142458757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a58ba916a2315dd545b33d49116270894e1fe2cba1d9f159dfbd0edf73bd34`  
		Last Modified: Mon, 22 Sep 2025 22:18:11 GMT  
		Size: 71.8 MB (71804729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ddaa4f8fa0b1323c4443965572b879d8b557f7fbd9c90953b6bb71cc5fd0484`  
		Last Modified: Mon, 22 Sep 2025 22:18:04 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:52afc2b1803fdec81a1359c4700ab6bee76cfbb50334fde1d92a156d89cd25bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a6436d9a9218c69a4695d9f186c0801129fd8d3e096f6a79c254612496754f6`

```dockerfile
```

-	Layers:
	-	`sha256:477770964280d6614d903f335f9765d614195419a8ee81f9d06f46b9e9b66ce6`  
		Last Modified: Tue, 23 Sep 2025 00:37:03 GMT  
		Size: 5.3 MB (5282641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:485ec016bc1d203f0d4c41e0dbc931f82e9c6d7a9230f907e019a420018b9500`  
		Last Modified: Tue, 23 Sep 2025 00:37:05 GMT  
		Size: 14.4 KB (14403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:13dc65236c46dcb657ed89c47f2a34bb2a0befbe7017ccd5c6fea016ca8c940c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.9 MB (243853541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9520c20af4770be6e6d89453d7072de7a43dc3e4c5d50bc066abe4f253f827c4`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f8526d99d3f421965f3fff0a7cbeeb99bb2e9969c47a3fbd1ff8b86c50ed59`  
		Last Modified: Tue, 16 Sep 2025 00:48:17 GMT  
		Size: 132.9 MB (132852835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9601431b4528b6deeb98906e5ffc5efbc416c72843417c47cd798fec2d4ecac4`  
		Last Modified: Mon, 22 Sep 2025 22:57:14 GMT  
		Size: 77.4 MB (77405710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3341ae857e901f5eee2ab1816ab5d98438023e4b7746955bd8cee589f713be5`  
		Last Modified: Mon, 22 Sep 2025 22:56:56 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9d4a3b8e39e9e1c1e18877521b8968fab85b79c76dd51ede3315a4e0ce852cf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5294344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc9d0b8ed1076c4b24888d37d90b1c63f934217f1a61bf8590816d9a0a10761`

```dockerfile
```

-	Layers:
	-	`sha256:0dc290e95fcf52243ae2d30f73cabc8a5d03bf5e7bb500d5209cea0b22934dae`  
		Last Modified: Tue, 23 Sep 2025 00:37:10 GMT  
		Size: 5.3 MB (5280010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:978d113316b38cd904de28efb52f93f9d04e737bf8b5cebb49981d26c46adb04`  
		Last Modified: Tue, 23 Sep 2025 00:37:11 GMT  
		Size: 14.3 KB (14334 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:31191881f109e145b1dddbe520886177783c309ceb1690d0c6a6bb32d5d60b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228411478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5d34703377986b34019a60b9814427f23e8d544b65a7360b254cfbafd7f799e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d713efc7a1d4629371af1ca545cf69623dde10f209e01f82c7ce9eb975cd5f`  
		Last Modified: Tue, 16 Sep 2025 00:21:12 GMT  
		Size: 125.6 MB (125622240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe76b962676e6e3ad174d3ebde9087b541197a3bd217a5598c0e8d0b1219f39a`  
		Last Modified: Mon, 22 Sep 2025 23:04:56 GMT  
		Size: 73.0 MB (72955688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa4d4928a54c9acc54cec65296b8c852669ed59c74379bff1dad4e6cbce4196`  
		Last Modified: Mon, 22 Sep 2025 23:04:53 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:42b9b3588be04841b56c878a4692fd252b80ae8a74a1a3bb0325065c3890d552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5286467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446f27681ac53a79415181c7b25a2f1623a9d46a6e233cd29a532ae6dbe38970`

```dockerfile
```

-	Layers:
	-	`sha256:cd6b55aa2da2a4968a71617cafb226cd9c5c28d17834be9c4b468d857e7a73ee`  
		Last Modified: Tue, 23 Sep 2025 00:37:16 GMT  
		Size: 5.3 MB (5272182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0086000023b1e2b5b0232584f28bb2dd8a3762c11b1a20c69f97faeac59769cb`  
		Last Modified: Tue, 23 Sep 2025 00:37:17 GMT  
		Size: 14.3 KB (14285 bytes)  
		MIME: application/vnd.in-toto+json
