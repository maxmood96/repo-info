## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:f68874918fb94c456a9fad82dbeb54e19de7c7c249b6f5d16a7c0299100303b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:aaaf38adc16668a60f0b6199c6285b2968ce75b9568f1f53018699213fa03323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.9 MB (267859440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a134cc037936ef271a97e9edad6e9257006592f1659f4b8227483e25214e6d2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:078965fc7cf303b72cc4eef5479dc2dbf5bc84fb8e6052a89b9b5362e14b3651`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 53.8 MB (53755344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e54a1eed49ae916f310dc11c085684acbea8de17d2515c1645d56efe9753e0`  
		Last Modified: Thu, 14 Aug 2025 03:04:15 GMT  
		Size: 144.7 MB (144693262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ceca132cfa9339351dae329a5b3671ec945cfb1965dfb0f33f0317990acc22`  
		Last Modified: Thu, 14 Aug 2025 03:04:09 GMT  
		Size: 69.4 MB (69409795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f909d273463b8965068cd07770332ed2dd718c639b02bb800acbd12dbc51e62e`  
		Last Modified: Wed, 13 Aug 2025 03:31:02 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63195bcf50f388a4c09ecc7ce82b32334dc87b2c2700f7f02770cfbae1d172ea`  
		Last Modified: Wed, 13 Aug 2025 03:23:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:80df4d3e9c4506d211a8704d8aeec03a5c17cc57a2820a93e9e815e0c5a5bf39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7411459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28b4322e045dd10aa360d0b193938429d162bb5d51c015d3bef5fc063a80e744`

```dockerfile
```

-	Layers:
	-	`sha256:1a215958d08091e76c457ac4716d528d74bb1464227824afcf1414e940e5bca1`  
		Last Modified: Wed, 13 Aug 2025 00:36:53 GMT  
		Size: 7.4 MB (7395638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee0a0c3690bc89db117fad157264fc0c88b544e91e574bcdb8c2286dd0e38af3`  
		Last Modified: Wed, 13 Aug 2025 00:36:54 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:87a2fcfe84975f35e739619a5d29d4b762e4c1012b5f1d08a42a4753bfd84d1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.3 MB (265329065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c55dcc79dbc7a5d421b003cb21310dd967e7c8b5ac75d09b883fcec6f8aa06e5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7b68ea47bc3cd8615e51fdbe0976cb4999ba56ce8764e755543a4521d69a32f6`  
		Last Modified: Tue, 12 Aug 2025 22:08:57 GMT  
		Size: 52.2 MB (52248409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd2f0f1d0a07a36a51fce77cb15b612a921dd938731be8b79205f084cb868af`  
		Last Modified: Sun, 17 Aug 2025 10:11:34 GMT  
		Size: 143.5 MB (143542120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f307d729e7f4766ac42ad22b3d4dca493432117ca1c9769a4d9d386c63c80d8`  
		Last Modified: Sun, 17 Aug 2025 10:11:32 GMT  
		Size: 69.5 MB (69537496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e329f4976a72dcc259599830b5e4be9c47f4326ab678d619291a65d7b0ad2c`  
		Last Modified: Wed, 13 Aug 2025 14:27:58 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8da4abdb144e0a4e63afb8780580171f2cbae4bef684ea44665f7ec7a3038a5`  
		Last Modified: Wed, 13 Aug 2025 14:27:59 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:899b559199963d8d5b3880e33aa93144e01f260d001678621709d6a0188cf6b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7416676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e79e2c47179b986cba2f543317260f9174b4c06600c4af52931cb91b2f9b31`

```dockerfile
```

-	Layers:
	-	`sha256:a2c85b24203be633dcabfce1bd5e6162d2a848ce79e867d5de2c737580617324`  
		Last Modified: Wed, 13 Aug 2025 15:37:06 GMT  
		Size: 7.4 MB (7400737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92a05c97bd9a2d16341681c3d8adefba65226e4849e5d984d6f51e04b890884f`  
		Last Modified: Wed, 13 Aug 2025 15:37:07 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
