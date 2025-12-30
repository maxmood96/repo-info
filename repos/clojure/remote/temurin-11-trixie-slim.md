## `clojure:temurin-11-trixie-slim`

```console
$ docker pull clojure@sha256:0d2401767c73e1db1036e21ddfe22afeaf1f9155bc9aaba9a3894da971e78390
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

### `clojure:temurin-11-trixie-slim` - unknown; unknown

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

### `clojure:temurin-11-trixie-slim` - linux; arm64 variant v8

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

### `clojure:temurin-11-trixie-slim` - unknown; unknown

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

### `clojure:temurin-11-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:a7385e0bec1e0e81f2c73d45a12d4108cb395e906833648331e4a38356f7c4a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243066244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17fa36112029a2e89f84eb2298e1dc543e102e1f5484d2be3d1e397202295a48`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 03:49:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 03:49:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 03:49:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 03:49:47 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 09 Dec 2025 03:49:48 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:53:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:53:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:53:37 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79c7c03426c1aec44b221775d1d53747ec67f1e33a2616e70c690b2a6e30b72`  
		Last Modified: Tue, 09 Dec 2025 04:03:19 GMT  
		Size: 132.1 MB (132081973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300f8b9360abd46f7a61ab51e3afa40f82a7a88748029bc276cb646388646378`  
		Last Modified: Thu, 11 Dec 2025 22:54:34 GMT  
		Size: 77.4 MB (77386736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5e50d9430ef2780657496dd06d67356b7b3375c70b168ba4467d6ed34d0097`  
		Last Modified: Thu, 11 Dec 2025 22:54:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:42c2a414bfb780cb216c7b953b14d960779717c08ddce14e6fed5869c613e362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5294385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0ee6d7146cad01f794ef96e24650470a2fd0d700cd06af6011d5a863358494`

```dockerfile
```

-	Layers:
	-	`sha256:10fdd9a1b238304e7dbcee92d2b02730bbdbd8fc6a65f380ec07bf2875426eff`  
		Last Modified: Fri, 12 Dec 2025 01:37:08 GMT  
		Size: 5.3 MB (5280094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a48c5955e7bc2c697ba4f9a30aa7404a328b69ca57d47cc0666e88e8cfb9656a`  
		Last Modified: Fri, 12 Dec 2025 01:37:09 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; s390x

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

### `clojure:temurin-11-trixie-slim` - unknown; unknown

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
