## `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye`

```console
$ docker pull clojure@sha256:edd78bf739abfbbb4dfd33b12dd9ea4f2f5975c5c052241603ecfd136bd3a8c5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e4fb16fe928735111d831839c9066af2f9c971c71e000faccbfe81a258d11bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269247689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ceced179c6670e4106da82a1acf3393045aa7c5a9ab9fec98da909cf165f9a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:06:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:06:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:06:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:06:47 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:06:47 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:07:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:07:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:07:02 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:54a03544060169d4b3f081ec8b02433016510da63c54baa3c2da97d8d0f1e9cc`  
		Last Modified: Wed, 22 Apr 2026 00:16:31 GMT  
		Size: 53.8 MB (53763152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5263c270395a65bf5aaf0994b43ed80d511a1f8e7362ab7e392aae16af6e0c8e`  
		Last Modified: Fri, 08 May 2026 00:07:25 GMT  
		Size: 145.9 MB (145886193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00618c12d93e94e9d5f4d3ed6d78d83de11594d21231e3e3a4d94dc547e877cd`  
		Last Modified: Fri, 08 May 2026 00:07:23 GMT  
		Size: 69.6 MB (69597698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7aada3300e75f019af82bc333c1dd8c91f89e2951200b3291c2442379c8d2f`  
		Last Modified: Fri, 08 May 2026 00:07:20 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f32b449e62ecd56ec72cabde532059b7ded3a36c1034586e57b7b6f14f8a8108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7442159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64130af217060e5d24a98eb05fd078aea692b19b12c5d82edded25b3ccf22cc`

```dockerfile
```

-	Layers:
	-	`sha256:efc3a315ceaa1fda3ec95d102f03222adb7770f446164dd65b42fd954e968e47`  
		Last Modified: Fri, 08 May 2026 00:07:20 GMT  
		Size: 7.4 MB (7427796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b965ca94b806fc564b902bc5c8449893431d263667399e29844bbe768d07d0ab`  
		Last Modified: Fri, 08 May 2026 00:07:20 GMT  
		Size: 14.4 KB (14363 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e76cda4326d1661539df4a626933f0faaf2f34cc6c5e0bc6f069d33fbcbd8c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.6 MB (264574448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1abf1a066e4e776a7572c1db286638eea8433b00ba40c503d5be3e0c654a0a78`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:08:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:08:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:08:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:08:29 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:08:29 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:08:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:08:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:08:43 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b2b472999165028200a3763e277d5915819d29f4cc156a7db994c22c536d04`  
		Last Modified: Fri, 08 May 2026 00:09:06 GMT  
		Size: 142.6 MB (142582234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401851b02362d66fc4a11079696601f6f3ff8bfc6cacff083a851d1d3ccb33b1`  
		Last Modified: Fri, 08 May 2026 00:09:05 GMT  
		Size: 69.7 MB (69738567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b5323971727ef8f52876857e5ddb52eec6fac815b8fa60ce455bf04440bd46`  
		Last Modified: Fri, 08 May 2026 00:09:02 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e520c2835e1864535e1208a01db45aabeb3e48a5fee7574e09700cb765bd3a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7447994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e14e230e75fffe66b3f5f3ecb006fd7c2a84761590ea9935876986075d1320e`

```dockerfile
```

-	Layers:
	-	`sha256:6ea95fad4bd0744dc94f0e961a391ae23136be1888d23dd99a7a63f1820edb67`  
		Last Modified: Fri, 08 May 2026 00:09:02 GMT  
		Size: 7.4 MB (7433513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68cc0afd0da4ffbbd9120d021e345a31c9a77c0f933dab230bf60020831f0d1f`  
		Last Modified: Fri, 08 May 2026 00:09:02 GMT  
		Size: 14.5 KB (14481 bytes)  
		MIME: application/vnd.in-toto+json
