## `clojure:temurin-11-tools-deps-1.12.4.1582-trixie-slim`

```console
$ docker pull clojure@sha256:688bae6f646b2319f0b5ecf588fe3a8d7baa603ed38ec8327eeb12b858b4c087
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

### `clojure:temurin-11-tools-deps-1.12.4.1582-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d6efbfb6836a1db269a684997bea865012233ad385e38e8a2cb5598358fda3ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246736567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6523afd7fa8c0503b5280fc02261cef00ba599fbec2db6662efd4abf391f51e1`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:55:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:55:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:55:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:55:15 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 00:55:15 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:57:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 00:57:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 00:57:27 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e322c43c95531fcf58008dd1b162b446869a807a77ede69728bb565029d0269`  
		Last Modified: Tue, 30 Dec 2025 00:56:20 GMT  
		Size: 145.0 MB (144966652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421106723cb44d6cd3f46833f89c48d440a9ea56089fd18817ea1cbe10b20879`  
		Last Modified: Tue, 30 Dec 2025 00:57:56 GMT  
		Size: 72.0 MB (71992738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3341843bb4ca4e658b4890bc010a08abd737b223c1e7b84a1d9265ad1f78468`  
		Last Modified: Tue, 30 Dec 2025 00:57:49 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1582-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:36043d50dd8cf794a183a0162ba0da398f0185f1debbdada2a876f28b940bd13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c30b273e0905f2141ef68d465cd2d73ec06544261573d4dbcc0aa87d5379680`

```dockerfile
```

-	Layers:
	-	`sha256:ef0fe2c28910d9ea900e91609861e27c1d9b42b75f7960cb1590c14a9fecb198`  
		Last Modified: Tue, 30 Dec 2025 04:38:45 GMT  
		Size: 5.3 MB (5276338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cdfb22b32aef432763bca51674502fe7af4b6468d523319ec1ece38edcd5853`  
		Last Modified: Tue, 30 Dec 2025 04:38:46 GMT  
		Size: 13.4 KB (13442 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1582-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f19c10357f82be2d7087a23ce4253085583f733b82cc109dfe3e9cc4deacc0dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243677306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2608d7fef759754b583cdcf16b6302cfd5c7dd331219af2ad0a8c0a3fd996a0c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:58:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:58:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:58:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:58:20 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 00:58:20 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:58:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 00:58:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 00:58:39 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e840da1433e778911e0157577bc8768532c48b0c6abdc01d32c72ef497f075a`  
		Last Modified: Tue, 30 Dec 2025 00:59:18 GMT  
		Size: 141.7 MB (141731502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1536ef631a4dc5b632d4f2b114efff64894dbdc3ca35d3614d6f06f9b4d044`  
		Last Modified: Tue, 30 Dec 2025 00:59:12 GMT  
		Size: 71.8 MB (71806524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cec75125c51e0110b31ba1d619c46d810de8a0329b408881161fcf0be0ef57c`  
		Last Modified: Tue, 30 Dec 2025 00:59:07 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1582-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a30097c022d7031971d437b6cd81379d6c4d5b52617a56ac616bac0633eca9c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48827a7fb1f4dbc78335e5683cd3f29cb5bbb6ea443fda349117246822807637`

```dockerfile
```

-	Layers:
	-	`sha256:d4257ed46d3efa464c0c4245ef121e83f6b89a7f6b580057e78efe8576d641bb`  
		Last Modified: Tue, 30 Dec 2025 04:38:51 GMT  
		Size: 5.3 MB (5282725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a36c246bc48097f323ef2a5d1f3b8ee854da0d535d737fe5c5586b701c230cb5`  
		Last Modified: Tue, 30 Dec 2025 04:38:52 GMT  
		Size: 14.4 KB (14360 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1582-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:aaceb829001a193b4fb6456fd1cac8009c7a3b1ed8043f8e63d04174b075188f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243066316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a4fb1eb8290a42d86abb74f353ab72126386c3e9f81d88f1aa0caa07b7003c6`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 19:07:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 19:07:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 19:07:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 19:07:54 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 19:07:55 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 19:08:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 19:08:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 19:08:45 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:34b56ab3c5579c93222f3403d640c7a7f19044e9e46a2d1c6b1da60bde918efc`  
		Last Modified: Tue, 30 Dec 2025 15:11:02 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cf28f764c2e28a5292338b5c0ca4db8c991fe900f886b5b721adc6ce62ec4b`  
		Last Modified: Tue, 30 Dec 2025 19:09:47 GMT  
		Size: 132.1 MB (132081972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819fc9bb660935ba25f12bf31a5e0a3dab0001e5d7d5e1fd721c3c87558f9d19`  
		Last Modified: Tue, 30 Dec 2025 19:09:40 GMT  
		Size: 77.4 MB (77386809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afcd587dba2f946264842417ad9475196e261edaa7fe14276995056c81336ba`  
		Last Modified: Tue, 30 Dec 2025 19:09:34 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1582-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:82f1b6d4e62a26daff174b02243d32c418506673a5a082d8c597af567227ce23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5294385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c530ee00c2a688d1eafad1a5f7445003204e85a1cb19c800f471465f222b53`

```dockerfile
```

-	Layers:
	-	`sha256:8a80f880740499b6e55561e5b81554b923f7c87e3c7238ae0db74f2b43de174e`  
		Last Modified: Tue, 30 Dec 2025 22:35:17 GMT  
		Size: 5.3 MB (5280094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:922bba9bff0ae759f5e79ca0a64e7d4e655d1961d470e79bdf695871a5e2e5b4`  
		Last Modified: Tue, 30 Dec 2025 22:35:17 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1582-trixie-slim` - linux; s390x

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

### `clojure:temurin-11-tools-deps-1.12.4.1582-trixie-slim` - unknown; unknown

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
