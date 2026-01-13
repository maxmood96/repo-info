## `clojure:temurin-11-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:6a054ed3a99cf937307ecc9b509b3810b46d759f647e851d2b9c8f90fd86181c
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

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:463b0385e1416f8a31d34028de1402c77e190e03a21a2d780d73ffe09bdbbcb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246734484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3f7ce0bbea467a45261e1d342e77d06d857a32d31404d94998108878d4bba9`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:29:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:29:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:29:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:29:15 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:29:16 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:29:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:29:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:29:32 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78cc866da93b5bd6e5043d070f75cd3dd836aa00a8a03e056eb8cde790c51bf9`  
		Last Modified: Tue, 13 Jan 2026 03:30:18 GMT  
		Size: 145.0 MB (144966651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725775530c096b7f4d582feaa0ce075d2608a058c97f1f9ae4a6edf9122ccc3f`  
		Last Modified: Tue, 13 Jan 2026 03:30:09 GMT  
		Size: 72.0 MB (71993502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db928552a59f61e69ede7cbae5f4fe3fbc67169519a6679643ee2e124210db1`  
		Last Modified: Tue, 13 Jan 2026 03:29:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f7d1055869d60ea190215892ee4a1ad6b524304ae041ef1e0e03c57dfc4ad526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5290679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ccfe1c1e8ba25fb32a7de97786c13e3ff84429a42b242e09a14a0bf70cbdfe`

```dockerfile
```

-	Layers:
	-	`sha256:c0abeb0ee6b6cb0617e9f2bcc76af53ea9e05751d3e823f4624e22172c23fe1a`  
		Last Modified: Tue, 13 Jan 2026 07:38:45 GMT  
		Size: 5.3 MB (5276436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed2849da1cef9da0c3aa0d06825e85d93b070db6fb75e2ba273bd1343dff6007`  
		Last Modified: Tue, 13 Jan 2026 07:38:46 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:afbcd57423de95f1c50185e1541ab8a2e5a2c9545218a91953d4e73244ca00bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243672369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b61f654bb69931ac038c6c5a8bea2334f7bc82e3617d4a9b9790cf9149ebcf6e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:32:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:32:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:32:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:32:32 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:32:32 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:32:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:32:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:32:50 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27d97467e7b0a89c1bbb3480fa2ed91002a5bff64a57083214bf5aae295b9f2`  
		Last Modified: Tue, 13 Jan 2026 03:33:13 GMT  
		Size: 141.7 MB (141731575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cfa83a09526a371fce94c6643705edbdc95bc604863538716f8531f8b771ba`  
		Last Modified: Tue, 13 Jan 2026 03:33:25 GMT  
		Size: 71.8 MB (71806108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced46b375d60314e7d22aa47338cd0ac0f52e0fab98339f2aae488ae5929b723`  
		Last Modified: Tue, 13 Jan 2026 03:33:18 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3bc9703c7e9740299ec917ca214c05ffd58eeccd8b54d2790992d69dde7e4036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d05f902ebc8a91d783b9e023e1f0acdd7a02f7d5342aa0984564f508c583d0c`

```dockerfile
```

-	Layers:
	-	`sha256:eb4e196176f8ef2a1d62c09e9c14f0bb7ba337b10056fd06cfc9aabd68549258`  
		Last Modified: Tue, 13 Jan 2026 07:38:51 GMT  
		Size: 5.3 MB (5282823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bc3ae72a3f2fb7797fc5c4ce624f29675a2492a6e51cff93739d8593402119e`  
		Last Modified: Tue, 13 Jan 2026 07:38:52 GMT  
		Size: 14.4 KB (14361 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:5fbe220cd32c9824dae0d03e0ff21b6e4d6c3e5ca5b94c6d6da62b14351f2096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243068192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97491dc554f156cb178320c4e2ec311bfab1e2555e0c2f3f813a85687aa9426`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 05:38:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 05:38:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 05:38:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 05:38:08 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 05:38:09 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 05:41:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 05:41:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 05:41:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:13 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e67d402cdd431289d747055012c60263964e508ffd51c9c226729bf26f2231`  
		Last Modified: Tue, 13 Jan 2026 05:47:27 GMT  
		Size: 132.1 MB (132081973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf48c40f4bab1fa337770be5a51a7a7f7a5e654645b02951253a2111c1355fa9`  
		Last Modified: Tue, 13 Jan 2026 05:42:12 GMT  
		Size: 77.4 MB (77389974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17c86861f8eebcb07c9298b654a970bb823039933fe56f696272a03fdbcbfbc`  
		Last Modified: Tue, 13 Jan 2026 05:42:08 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9bcbf63848de0c750d604153b88f52f6ba728e104d30d3b40a313fc7227e085b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5293681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca99bb0459adcb96de9bcd4a719883476e5b9a7ea2c8fd1967305a16c96c624`

```dockerfile
```

-	Layers:
	-	`sha256:aabfbc2d40bcf07947f6c8f26b6a7d6e8deb163e984cb0fa58fda31097a9ddde`  
		Last Modified: Tue, 13 Jan 2026 07:38:57 GMT  
		Size: 5.3 MB (5280192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1059788f5dc9033998522784c0d949c0cf3cf96c9ab1fdefec362fb3f43e15dd`  
		Last Modified: Tue, 13 Jan 2026 07:39:14 GMT  
		Size: 13.5 KB (13489 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:4170ac1025e12a9a4c46e8a21563ea87ca2bafd8192b4f7de4bac0d971374fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228483139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f85a67d36a1344dc189a2ccc336d2cf4cc8599ee60dfe2f618220f0c3a0c4f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 02:01:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 02:01:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 02:01:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 02:01:28 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 02:01:28 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 02:01:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 02:01:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 02:01:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2169a9d601723761e7ce429e1caeb35d7b1ff57ebd897efad3c22fd3f8a79d0`  
		Last Modified: Tue, 30 Dec 2025 02:02:32 GMT  
		Size: 125.7 MB (125694401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2b8324539c6d3c4817f9f7865f2749a04064cbfb6a36f52b8ec7070bb7e1d0`  
		Last Modified: Tue, 30 Dec 2025 02:02:30 GMT  
		Size: 73.0 MB (72953676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d8d96df6e521bd80f285635f4701aef54c2a225b88abafa61abeae58f6d813`  
		Last Modified: Tue, 30 Dec 2025 02:02:19 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8019b5c09c8666a4c06f0575547f39b7205787f71e443ab9bb52021f13421dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5286509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93e483247abacbdf00e5d2b3d704de5209abe0d54bf328a14589e5fae60fc112`

```dockerfile
```

-	Layers:
	-	`sha256:69db853cae35edac706a1a6a8b07e1da066aa8d8ef89543fb5dc9a6754d40a72`  
		Last Modified: Tue, 30 Dec 2025 04:39:00 GMT  
		Size: 5.3 MB (5272266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6391b720841b38310b2924b146004d919db5d83a3ca49a8e153b3582c478c5bf`  
		Last Modified: Tue, 30 Dec 2025 04:39:00 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json
