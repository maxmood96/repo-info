## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:c0c53c5a28b67d5cea8928ba3195bdd6257c7ecad496ba093f596a9ed72b1af9
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

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1615e194589155c7112435a927324d8a1a149ad2bed3c8ac2460cfacd36f4460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243535457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e85f5da9b8411a7409335268efc2866a05bfd6fb9a9757ff343b0dbfe738c1b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:03:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:03:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:03:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:03:39 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:03:40 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:04:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:04:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:04:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:04:54 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:04:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68d974786d34e9bfd19528b4b7d140d4750db75a0ee380aab54d0bcc7371a72`  
		Last Modified: Thu, 05 Feb 2026 23:04:33 GMT  
		Size: 145.6 MB (145628407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1338626375683b39ee9cb4a8b35cb1457b505a12317d1306edb6580a9df7447`  
		Last Modified: Thu, 05 Feb 2026 23:05:11 GMT  
		Size: 69.7 MB (69677519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0566cfecaa63e18b187d8dde556767bf12ca38a016ca665a28c30d337648b482`  
		Last Modified: Thu, 05 Feb 2026 23:05:09 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc57226488cbad926f363d9874c04810ee827f32f7a398917ea81c6974425d23`  
		Last Modified: Thu, 05 Feb 2026 23:05:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:12dea320479432209366d57b298166a65dc200ff8d2f6d641968959847770bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5130490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c389024eea3fb92c0e55b7c6884c5af16dfb17323c29252089a5c9e500ee87c3`

```dockerfile
```

-	Layers:
	-	`sha256:8bff11a257b8cfb16cba8e58eddada7bc916383eebb7f65eb7fb18b604580ca9`  
		Last Modified: Thu, 05 Feb 2026 23:05:09 GMT  
		Size: 5.1 MB (5114654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef8e9088cb72dc9500dbfcfe582033d833e09a3aa607c066ab8483a16b1bd26`  
		Last Modified: Thu, 05 Feb 2026 23:05:09 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8672972437f0ad62e6f5653296c60317039d7dd71637a5dbbcfe448c2de1b272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.2 MB (242217663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60df0ac27088de5a5b1cc3d0d923b9f048d842579cde26314fb7d61ce91d8925`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:05:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:05:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:05:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:05:44 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:05:44 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:05:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:05:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:05:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:05:59 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:05:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb57f885cdee6ae41a93931f75adf38d811b81f7ca2c8e2d1ad6b2d7fbd47b5`  
		Last Modified: Thu, 05 Feb 2026 23:06:22 GMT  
		Size: 144.4 MB (144436240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52221064604660a111d370e2eed129770a59fcb6ff384b02537a6d14270d31ca`  
		Last Modified: Thu, 05 Feb 2026 23:06:21 GMT  
		Size: 69.7 MB (69672556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2e91675e150652dcefb8e33ee5e0810ff8a31a2c5048afaa30d16a2179b92d`  
		Last Modified: Thu, 05 Feb 2026 23:06:18 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825ce7fec367d2736bade312ba5587a895bb5a438266f9edf52a749fad173091`  
		Last Modified: Thu, 05 Feb 2026 23:06:18 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:514700245ffac71616dcfb9b3b227b47a97f2f641dc119b20e5fd88791396433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5136369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c21656ef1d5086930258dccfc50e90f52e9a99d12a8c7bcb5cce0bd3b98746`

```dockerfile
```

-	Layers:
	-	`sha256:5be8c99c1b4f9ef9d5313e95116be948380ed23b1b0d923338c30bc51b7510ee`  
		Last Modified: Thu, 05 Feb 2026 23:06:18 GMT  
		Size: 5.1 MB (5120415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce8471176e9d37b337248428f1f51b719a8339f1bcb9e991ad84828b283d1663`  
		Last Modified: Thu, 05 Feb 2026 23:06:18 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:030fd79bc9cd4f2603f4634559fb864d223b2e0ba08547911525920850f7279d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (253022171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f9aba1095b8d610e20cb59a335d9b2f90881a9ae1ec0c0b7cf8479fcc7e62d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Fri, 06 Feb 2026 00:22:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:22:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:22:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:22:02 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Fri, 06 Feb 2026 00:22:04 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:28:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:29:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:29:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:29:02 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:29:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7910825c7ec7b68916beacd9af906d34dec10e730af19f67c87aa4e2ee440381`  
		Last Modified: Tue, 03 Feb 2026 01:12:56 GMT  
		Size: 32.1 MB (32068712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56445963f10f9073db32d8e55af4130cabe6e777336d5f50276061d989325f1a`  
		Last Modified: Fri, 06 Feb 2026 00:23:46 GMT  
		Size: 145.4 MB (145438231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7aa19b54159e662764c554974ee7bcf22a2cbb38eaa8dc57a0b6172871f8d8e`  
		Last Modified: Fri, 06 Feb 2026 00:29:49 GMT  
		Size: 75.5 MB (75514185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977176e520a8d8e543e6f990a43ed054ab1ec4aa4c6d7b388021533b72907c7b`  
		Last Modified: Fri, 06 Feb 2026 00:29:47 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e75b55894808d63b4dcbbf02aece8bb1c7b172eb9eea15eca37751dcc63acf3`  
		Last Modified: Fri, 06 Feb 2026 00:29:47 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:da81d45d3890cd7ba63622867d49b666f50cad03ef76f60648c8c3eaa1fb247f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afb1da38fa077c33377a5bc379a51b802fd4c931358b6bbd76630eb71144111`

```dockerfile
```

-	Layers:
	-	`sha256:1b93d76c5080df3c51aa6680be864b27493658238675a670a4d25daac14379d1`  
		Last Modified: Fri, 06 Feb 2026 00:29:47 GMT  
		Size: 5.1 MB (5119812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ccc7c11c3b5d358facd6651e4bbc85c491f4222f6e1b885efc7509fc4162d91`  
		Last Modified: Fri, 06 Feb 2026 00:29:47 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:361041745ddd36964333165b144a5b5a9444c9662fe1e8daffee0e956063af2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231002455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d427e13ae11333482f8819920fda4843c28e6cbebd27672ad1547e7b62822479`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:01:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:01:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:01:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:01:57 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:01:57 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:04:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:04:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:04:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:04:15 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:04:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af58cc4761e637c6263de1747b7d56f05c86d8d94c69c1d5359a66432b8c048`  
		Last Modified: Thu, 05 Feb 2026 23:02:41 GMT  
		Size: 135.6 MB (135627055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01411b9f0319e393c520ce01bb7255e61cefae14cc7bcee315f7a3adf75e0978`  
		Last Modified: Thu, 05 Feb 2026 23:04:40 GMT  
		Size: 68.5 MB (68489975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda0c92a77fd0f1c53cebaeeb46cd16288f1e2a319679eb71f3d889f2fd2a089`  
		Last Modified: Thu, 05 Feb 2026 23:04:39 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad60b7a2d5779fb735da4db70c62e66ba3eb468f5fba80695e6c232456417fc`  
		Last Modified: Thu, 05 Feb 2026 23:04:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:af5aafd5aad8f873d2c5fad890bf12e13ebe8f64d6b5211cb2981032ff8f7df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5121811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a3ab09aaabb90d21c221760aad3c3ec9699809aafbe35ae7b9eff5a8f71365`

```dockerfile
```

-	Layers:
	-	`sha256:16ad59152bc66ad18d705a157bb314ccf5e89bd7f7b53092f2e7bdc165713afa`  
		Last Modified: Thu, 05 Feb 2026 23:04:39 GMT  
		Size: 5.1 MB (5105975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7acc46b8fe265a3cf14509f8cfcd96c3135ef2f51004444dae32c3ffb05b5b66`  
		Last Modified: Thu, 05 Feb 2026 23:04:39 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json
