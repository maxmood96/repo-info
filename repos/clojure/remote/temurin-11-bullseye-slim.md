## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:4bf4b7da76fd35db0d990f116bf0d962401f2c6069e562f9e11371300905a795
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:44d64fe4c72765c2b42d239668dba3721c805bc4b10470cb577d1e9df397267a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.4 MB (234375404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883b8018f6bdf323fa21b7a7edf29af5904511f43430ea2d200a72cab58877b0`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 01:49:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:49:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:49:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:49:49 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:49:49 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:50:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 01:50:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 01:50:02 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:bd1b97a95a10ded4767bfcdbb3d042b961d107d141121fdbb255239f0ca115f4`  
		Last Modified: Tue, 13 Jan 2026 00:42:30 GMT  
		Size: 30.3 MB (30258497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25d0ea255f9a418518d098495143019088db7c9ff840ea5519859c0df2dc9b2`  
		Last Modified: Fri, 16 Jan 2026 01:50:23 GMT  
		Size: 145.0 MB (144966614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e0002c56cf28930a88220ffcfdf1e56a7facacc17645c27b09e2b1500cd6bd`  
		Last Modified: Fri, 16 Jan 2026 01:50:21 GMT  
		Size: 59.1 MB (59149650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ab92b31d57a1f4b1bed9408ec51a98e18d05fc85999a8e9c4255be4f141427`  
		Last Modified: Fri, 16 Jan 2026 01:50:19 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cccca64ee3a10937855a9dfb71c230dd085a27f2b4d46102a626d47edd3b7f80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5342475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28888092b72f22bc025e4d56afcafdd360c860a5682b8b1fbe60f88ffd98964b`

```dockerfile
```

-	Layers:
	-	`sha256:5261c422fe5b4b40a333219d8daf14a708498380fc3f2c465887f0496c1a8483`  
		Last Modified: Fri, 16 Jan 2026 04:36:59 GMT  
		Size: 5.3 MB (5328208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c4aff163cee672b95f4b5332558c1886f551a14f9f93fd1794670a63a8b90b2`  
		Last Modified: Fri, 16 Jan 2026 04:37:00 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a9dd28fb63fd455222c53dc4f84b72125389cfac086cf9c84f782be5e04c5fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229762854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87da93377d0591b0c523a3b1c9809f8f52a96ec013af962fa193bcb3c05c0e6f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 01:53:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:53:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:53:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:53:45 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:53:45 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:53:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 01:53:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 01:53:59 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:51 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47eb9835e2a541e1c96e259530cac07c2cabfb5c6a06f3793f5f1e348da7ec95`  
		Last Modified: Fri, 16 Jan 2026 01:54:20 GMT  
		Size: 141.7 MB (141729889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34845b157464d182f90c8e11e162b59b4712a0bbbbdd1dd1679b984229d3b595`  
		Last Modified: Fri, 16 Jan 2026 01:54:19 GMT  
		Size: 59.3 MB (59283801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e863789e19cca148c65d14f72fb173365d46c8001d7c544c252400a8149959`  
		Last Modified: Fri, 16 Jan 2026 01:54:27 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:40cebb73e9f4b2e42be5bb2731f64750799444bf989acaca12e6b851e7b2d4bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5348943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9865fac6eb9fd5c01e228349b465cfc9ae946e54820f93c703a6ce2bde3fd896`

```dockerfile
```

-	Layers:
	-	`sha256:5c8ed33e94d7ca49655d8e8f73ee0be6fd2fa7ee6642c81b03250b1ac057bf74`  
		Last Modified: Fri, 16 Jan 2026 01:54:16 GMT  
		Size: 5.3 MB (5334558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfbc0980549e1d88b389baf5bddbd038928cb4a2eb84669781e63dd4789750f4`  
		Last Modified: Fri, 16 Jan 2026 04:37:06 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json
