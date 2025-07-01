## `clojure:temurin-8-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:5533d1e0ffe1114a11eec1b96f7be68c785ffd338ab8a4be4708bfe33d0feee1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:faf831f2fecb2322c9105ebc68d066674ecd4d6f45f14abe4339a66abb90e4b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143978487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67dc410cd2223b944e8178449315eeb3c248d6dade5d1cfd84c6c28f09e1dddd`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317741e06158868e7eb9db56aa2712e0eb4de8f00c6fb79a16eab0ab77179192`  
		Last Modified: Tue, 01 Jul 2025 02:37:43 GMT  
		Size: 54.7 MB (54716160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b187713dbb703dd8d313f8b31ce5c2cd5bcf04eb12593d1ae2de0718f9d1d184`  
		Last Modified: Tue, 01 Jul 2025 02:37:40 GMT  
		Size: 59.0 MB (59005635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ef5995f954d7fe3a6d1c8972827731316c2f0e3ac26495a7a728be66442768`  
		Last Modified: Tue, 01 Jul 2025 02:37:36 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:185975fb93cce5e2aa2b4737a7f240a0e0929d683ed62ea866fd7c9fb2756103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5443938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af5ff3d5d15d69ccf4297e00cf881b36f6162b9f68e579b1399fcb4cfeb3833`

```dockerfile
```

-	Layers:
	-	`sha256:2c80e902d072c03c45c59f7c8ae0e03859f7b9d677eb5dc2f113b54f87b6eb64`  
		Last Modified: Tue, 01 Jul 2025 06:42:24 GMT  
		Size: 5.4 MB (5429648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3944392a24eb7f299d8c51e0a7a556e506891849bb31652427622c2b3af903f`  
		Last Modified: Tue, 01 Jul 2025 06:42:24 GMT  
		Size: 14.3 KB (14290 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fcb1edfdc64c63e3e65d1f81954be1acbac6dd68b485bbe2670c7744483222d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141712943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09ef2d7c01a55813ae6cb8813650da81d2fa201ea364b07536e0ae8f475dd19c`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:00ce3d02ade4a2c8e5e37b1a218bb5c24c995bd8757095b89316c42854286fe8`  
		Last Modified: Tue, 01 Jul 2025 01:15:35 GMT  
		Size: 28.7 MB (28744140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d6e24d7f1e2bf70cc8f256559067d78169e098c2009cc94fc9ded67b1a270f`  
		Last Modified: Tue, 01 Jul 2025 11:58:33 GMT  
		Size: 53.8 MB (53830491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778f7c41ecb6100b1cb4514565c1a5461816e4c251e37c3a6a515fb9b5e454ff`  
		Last Modified: Tue, 01 Jul 2025 13:21:38 GMT  
		Size: 59.1 MB (59137668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a86083a9d3aaf411cf2722844980a476227b850f48508bf44e42170de152b93`  
		Last Modified: Tue, 01 Jul 2025 12:03:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:62111382f0a0ee33aaf6b0915105541d389547c7f63bef2e6cd00b47e0a66cf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5450487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:261f83d1e7b9dc9e88c711f2a44736e63b90294564467eca3a9becc08d3627cb`

```dockerfile
```

-	Layers:
	-	`sha256:ec284e9f666e002a6a884a8c9d155a6f6f5aaab7b9f1df5f613c14f07cc98cea`  
		Last Modified: Tue, 01 Jul 2025 12:38:54 GMT  
		Size: 5.4 MB (5436078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf4037ceee672c1f60c27fd2da4790d9a53aeac7cc103ae723432b6c3a2d279e`  
		Last Modified: Tue, 01 Jul 2025 12:38:54 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json
