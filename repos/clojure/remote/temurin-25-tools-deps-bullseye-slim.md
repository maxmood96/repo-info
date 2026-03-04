## `clojure:temurin-25-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:690c2d083dcb256cb82cdf8b9cae359496b575b200f094170b33a26a5370f24f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:05c4eeabab59635367fd132ac5e0272ba66c99cc1c5a5a7d2a88bcb0516e5087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.7 MB (181699108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6be56c2236ff80c0f254ccd53cbe50403778600be4ba8a84c8aad651cfcdf5b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Wed, 04 Mar 2026 17:51:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:51:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:51:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:51:41 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:51:41 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:51:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:51:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:51:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:51:55 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:51:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:34f0642d22440b5813561cd4375937013bfb556bec8ff3b0e208699b786282a7`  
		Last Modified: Tue, 24 Feb 2026 18:43:06 GMT  
		Size: 30.3 MB (30258379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25aedc329c16203cf777afc5eb291a8fc2b98c9769979584b2a23c31fcde75b9`  
		Last Modified: Wed, 04 Mar 2026 17:52:15 GMT  
		Size: 92.3 MB (92256290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926887c762b7ea07b1fe6532447feae7061c89ff7ac214f083ff043f0af60ac3`  
		Last Modified: Wed, 04 Mar 2026 17:52:15 GMT  
		Size: 59.2 MB (59183397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc918ed2c1987c2c80e841f69b21765f8221412ac6f03d0e5d457f2b9a094f4`  
		Last Modified: Wed, 04 Mar 2026 17:52:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75798c9c58579534c5996c4d8334a9e4da7ddebcb718ee6346d3bbb6acd9883`  
		Last Modified: Wed, 04 Mar 2026 17:52:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5eccea0af166708a203cb34702c5696577d1200040e133c06ae20f1257e79eb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5306296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eedeb08cbed01750fe681b9b99e2be4357a48d7165f6ec9c95a3855b3fa93f3`

```dockerfile
```

-	Layers:
	-	`sha256:776d0a0d53eaa8e71936c7f9e6c90dbe2cb512e8ad0f26c919d816c918cd90b6`  
		Last Modified: Wed, 04 Mar 2026 17:52:13 GMT  
		Size: 5.3 MB (5289771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0c52bc1d67f0d50ada1eb3ec578f7be1c00a14768053318471ec09f973092b1`  
		Last Modified: Wed, 04 Mar 2026 17:52:12 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:879fbf07a0b89f18036de5cd7e4740cb5f0069628bfb9476dd58c23ef19bc64b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.4 MB (179357023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c331846dc1caa4bd93046f591e11ebd57ac036adf0d24462b46a88b3f1cbb77`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Wed, 04 Mar 2026 17:51:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:51:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:51:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:51:16 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:51:16 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:51:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:51:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:51:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:51:30 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:51:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:018c0693c4a2532e5636d6115333db6d882da8f33f1f40cb3e88dbe62da21aac`  
		Last Modified: Tue, 24 Feb 2026 18:42:36 GMT  
		Size: 28.7 MB (28744470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb04096f6433fad998cdb06a3e5f6681d7b4a1a83b597b8801911353a28a97c0`  
		Last Modified: Wed, 04 Mar 2026 17:51:51 GMT  
		Size: 91.3 MB (91288275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851587a4b5a72df405886c0a58b21c36ec10a5245b1a69b4ebda5e7b9faacbc9`  
		Last Modified: Wed, 04 Mar 2026 17:51:51 GMT  
		Size: 59.3 MB (59323239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb0466a81599904b5c24245bf132b02686093fd6c64b92777e55b7441540d3d`  
		Last Modified: Wed, 04 Mar 2026 17:51:48 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0b05c5099b3813d3a7bd7e87768f8201863d86e83b87710cf9fb7b1267c359`  
		Last Modified: Wed, 04 Mar 2026 17:51:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7082d139e2278e0f08cbc80524ecf55ede4cbc95b39e457da8fa794072efac7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5312191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd1a67f5f7f3a302b048380c47cbe0712e9bb38c00b8a1cc12b7a9aacee8308`

```dockerfile
```

-	Layers:
	-	`sha256:069aaf3706f49dfb0927ab5f2fd768cf78c5dd728d0f33a470dda2bd3bbeb375`  
		Last Modified: Wed, 04 Mar 2026 17:51:48 GMT  
		Size: 5.3 MB (5295524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:088a062c103f790f007869abc632da8ae5d4634d7daa3f9c95a4164aad06f4bb`  
		Last Modified: Wed, 04 Mar 2026 17:51:48 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json
