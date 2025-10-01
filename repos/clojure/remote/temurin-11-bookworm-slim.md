## `clojure:temurin-11-bookworm-slim`

```console
$ docker pull clojure@sha256:a9b78ec7104c2c2a4db5ab5afd4010455cd3e86ef145248670fc9e6efff0b098
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

### `clojure:temurin-11-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c8b9828037a0bbe95d36423ea749493c67b1d9cbb4a238a61b05c8cbd4828f6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243566803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e707c3913e2a3bede2eaf3ec03a37bb03528a95c6f524222a72a014dd1ca819a`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8363a44d43c5f395de9d4723727d4424faaff68b8854b1ef1ed819d57d77261e`  
		Last Modified: Tue, 30 Sep 2025 00:52:26 GMT  
		Size: 145.7 MB (145658246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d913a55fbc700a746fbb85b4ec328831363149734aa4c6ae30c249a1d113596f`  
		Last Modified: Tue, 30 Sep 2025 00:52:24 GMT  
		Size: 69.7 MB (69679578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706d810a80893cafbea359c274e4a59c33d2c1e540ab0aad60ad2265f956f783`  
		Last Modified: Tue, 30 Sep 2025 01:39:13 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:96c1f6303e978d8146fcd5e903ae074be62d08a12c7fcdcb856db192f7b57c34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5147839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:341faa9230943af32674cd29e9fcaf7d0be37b5fcec921089babc2d8c759f25b`

```dockerfile
```

-	Layers:
	-	`sha256:4651724ddb39fa4b499eaf2c1abc4d7d8d291b0e6bfbd98a74d9cfa1ef446f6e`  
		Last Modified: Wed, 01 Oct 2025 15:36:52 GMT  
		Size: 5.1 MB (5133529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4850fb7e9d443bb5c500fb919efe6cf4081985ab19bed9294e5bac9ed1c41d0`  
		Last Modified: Wed, 01 Oct 2025 15:36:53 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d0eae8d2edeafebffccb45fdf9566eeeba1992c4b9996542923f1c7feaa41790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.1 MB (240121662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d84e856eac8d8da977584663d65746e1c0b3c8f6371cf1fe13c8203a144ff7`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4879a468f4e899ff0919bbba0986b5b5bb3075c4b58e7c1677660cb8fa8a6ecf`  
		Last Modified: Sat, 27 Sep 2025 03:07:30 GMT  
		Size: 142.5 MB (142458757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab93e01ed72382c350d853dc970ef345a6b98a94b181c0f68c3b6adb4864b1e6`  
		Last Modified: Fri, 26 Sep 2025 17:54:30 GMT  
		Size: 69.6 MB (69560161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89d0120f665114070d7465296b46b64ab0711083ca42bdda8828a41a3f69a81`  
		Last Modified: Fri, 26 Sep 2025 17:54:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ab9ba2be1835e6bb51cb451c1f62b56247a856248fd962f1277b5c7e04ba2fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5154335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e4bfe13a4584778f3f8cd30d93156c3d18de48aa24600d2c5305263c9776b3`

```dockerfile
```

-	Layers:
	-	`sha256:1eb436183ebe06e62c0a998104774eefa00e569388ec9d8221565d2e88b3789c`  
		Last Modified: Fri, 26 Sep 2025 18:36:17 GMT  
		Size: 5.1 MB (5139908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8f7727e2804e05a137d456341ce5265c64e98b855e170bfff7f85fdfbfa8cc9`  
		Last Modified: Fri, 26 Sep 2025 18:36:18 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:7037973fe21eb413fe684139f1e361f8e4f61dc171228856f394a9f712d8c306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.4 MB (240435137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d011ab013e3a60f538c4a57135db60984979e1ddb4fc29bacd123efd00b7ceb`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a438293490bbc2af66661166949a4d86358eeb39f9fadd5b0146666f05b9b9ac`  
		Last Modified: Mon, 08 Sep 2025 21:30:47 GMT  
		Size: 32.1 MB (32068762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde66219dbd7a1c29f39eb4950d9507e2b19040de31556e72cf1cfad16a668bf`  
		Last Modified: Sat, 27 Sep 2025 20:05:09 GMT  
		Size: 132.9 MB (132852830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaaadcf5cdc2dccfa0bbb5d78c067c00a144276240ffe0a443e2d073a982beb3`  
		Last Modified: Sat, 27 Sep 2025 20:05:21 GMT  
		Size: 75.5 MB (75512900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea1f4fcdf81e5c303acbd86ab1e7411effa7502753ed16f15f03f4ff79f743a`  
		Last Modified: Fri, 26 Sep 2025 18:14:34 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:380ef63266554d193cb59e70c1daa0b971beebc1273d292c5210c166087f2565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5152430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b006c1cbe5e6232c51522638208fff7b30704df64922a77688c83e67731a56f1`

```dockerfile
```

-	Layers:
	-	`sha256:50bc311f14b79419101b6be493768daa502ce91ab767f9739495d5f17ca4ee33`  
		Last Modified: Fri, 26 Sep 2025 18:36:23 GMT  
		Size: 5.1 MB (5138072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bec18f00a53f8b14d8043cda484381404160ba6fef5cf919f327be4f0143087`  
		Last Modified: Fri, 26 Sep 2025 18:36:24 GMT  
		Size: 14.4 KB (14358 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:63d2ce86b0abd511f592931d7252cb57032a0882e9b07c9ccd3c3788b9c74670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 MB (220997535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:390a28d8ed3c9bca35db6646339aa4b52166011146ba455bec60ddb9b969501f`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4285530de7ec8917c4ff373f911565d4f63e7c26eb3f53d8f0b1f0cce80f15cf`  
		Last Modified: Tue, 30 Sep 2025 05:46:58 GMT  
		Size: 125.6 MB (125622246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e19f68ee71a40217537e55cadea4bf8c7931c3dc7ecf4ed5d6bae37e43f3758`  
		Last Modified: Tue, 30 Sep 2025 05:49:29 GMT  
		Size: 68.5 MB (68490327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d402c36693c56a6fddfc3648ee7cccb9ffd0a66ff0f1085b242766760b784eea`  
		Last Modified: Tue, 30 Sep 2025 05:49:22 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7b75a2023d613beef8154985bfb77a99d18852c226697ded5873e250907e8175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a673a3d69e7ea9d86b3e09798286d6e4cb9d92b40202e33ed429c7399ec18961`

```dockerfile
```

-	Layers:
	-	`sha256:0b2a8734f5d178bd18c5cfbdd5c2f295b6e819ef0317b74ddfd93effb01c4d2d`  
		Last Modified: Wed, 01 Oct 2025 00:34:43 GMT  
		Size: 5.1 MB (5124854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:899e0f4cdf1942d7b7e9009146a4c1da73097f71376ea70ce06bdc40f5021dc4`  
		Last Modified: Wed, 01 Oct 2025 00:34:43 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json
