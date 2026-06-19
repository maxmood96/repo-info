## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:44e7c306bf0bbcf6e31a2d6049d5e5cedacefdfefd45b49227fb180f5db6e258
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:a369d770397ef33eefe406e1dc083bafe4977970982808cc38fc38d466a081f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266170766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43cdae842b5eb1f2695b8eaa9ce52568532f153b9e46551cd8760df8ec4ededc`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:15:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:15:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:15:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:15:55 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:15:55 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:16:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:16:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:16:08 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:af48a3e7696e07f88a02f9674e541901b65eadb5cf0f62e566b1d895099a1e9e`  
		Last Modified: Wed, 10 Jun 2026 23:40:09 GMT  
		Size: 53.8 MB (53771769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b139be38763e67841b4b9784d2215b175e4c76c9b570463f69323d4a35ae91`  
		Last Modified: Fri, 19 Jun 2026 02:16:30 GMT  
		Size: 145.9 MB (145886130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbc6cf3bb78db962bb5beabe193ab5a83fc5908bb4f58fb7ac0674e85e27a63`  
		Last Modified: Fri, 19 Jun 2026 02:16:29 GMT  
		Size: 66.5 MB (66512223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb136e3e16779b346e5fa1a678493b17e5258a1f1236bee293ac3f1aaf070dd6`  
		Last Modified: Fri, 19 Jun 2026 02:16:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:cf846870cad186049b148c8ed0d8ab3ed77abf833fe46e33126a6c066ed4143a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7440951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad17dc2c42efee6b4c4d3ba02c5eac0b9749970aafe5f07204318d48384b597`

```dockerfile
```

-	Layers:
	-	`sha256:a6c4ab9a8efb441ac0a9ec82e561a94610f81be6326e3e02c0cdb5dbd66bfdbe`  
		Last Modified: Fri, 19 Jun 2026 02:16:27 GMT  
		Size: 7.4 MB (7426589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:496927f9e7febacffa64634b41bc4f9117dcfddd344dd548caf115a2856be035`  
		Last Modified: Fri, 19 Jun 2026 02:16:26 GMT  
		Size: 14.4 KB (14362 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d28c2713b72d0478b3ac917cc290183e9822d93a22ed63151c26a6c55fc09fbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261524894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d271a7dbd4ada623a2838469877dadfb4a148d6eaf336b9b4e56b8667b7f0e`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:15:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:15:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:15:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:15:59 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:15:59 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:16:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:16:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:16:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7c21e59e753cb91625909251110d6e4cc4a5411b4b7b37f74a62e56b927b7f1e`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 52.3 MB (52264114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40109f5abaf486ffe5ae999001730501f3807d587c82efb87d454dbb24a8e1f`  
		Last Modified: Fri, 19 Jun 2026 02:16:35 GMT  
		Size: 142.6 MB (142582140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eee364f1029374e8a462c18b1fdd75086c820017c28685e58421496112d6bd5`  
		Last Modified: Fri, 19 Jun 2026 02:16:34 GMT  
		Size: 66.7 MB (66677998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def25fa80e00ebbe2ec153e37db6fffb6f8f74ee1874bb1e754714236507a897`  
		Last Modified: Fri, 19 Jun 2026 02:16:31 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:14cf318d5e47697dadfc18d6235918f91efd7df1419cfde6955ee56009d1f724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7446787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fac622b42e06bd62510e9e735769816c7a58e8a2ba1c2d5a6f11dfd965c938e`

```dockerfile
```

-	Layers:
	-	`sha256:2ba8d3238570b5b7b89a8813f8ec0242cd58e2ed1ff8d98ef9243ff4a359fe6a`  
		Last Modified: Fri, 19 Jun 2026 02:16:31 GMT  
		Size: 7.4 MB (7432306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed2c476ccd9d7e17b8b4ae75ea47ffb1c4e0da85cd1ad988abba0a1da3e8c101`  
		Last Modified: Fri, 19 Jun 2026 02:16:31 GMT  
		Size: 14.5 KB (14481 bytes)  
		MIME: application/vnd.in-toto+json
