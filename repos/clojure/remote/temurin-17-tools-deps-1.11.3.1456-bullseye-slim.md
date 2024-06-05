## `clojure:temurin-17-tools-deps-1.11.3.1456-bullseye-slim`

```console
$ docker pull clojure@sha256:b344e59c19f14806163c0554de23c4aeab46aafc45c38c471c319e18d751c516
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.11.3.1456-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:74fd85bec4c9c560d680ff851561da69b8bce4edf6eac227851be5a1cb832006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234949678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aefb8c57395601bba07328ddae7809684954bd6e7454db9f45039122e2a5cbf3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d53c5e6c23a46d782bcc9fbfbc4a31966196c4e6f342a89ac67368772b96dc1`  
		Last Modified: Wed, 05 Jun 2024 06:10:15 GMT  
		Size: 145.1 MB (145095120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc68b5f5b34b61e770467b871c387d1c57c2026596b4030d5c6c32aa14adba5`  
		Last Modified: Wed, 05 Jun 2024 06:10:18 GMT  
		Size: 58.4 MB (58419580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1938cc39534343e7aaf6e15e5fc82ff185c9a0c583348e7ef81cc5d7ea8f23`  
		Last Modified: Wed, 05 Jun 2024 06:10:13 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dda125a3927da4a8666dc6937dcede5166d9883080e630c3e25d11b4ee65ca`  
		Last Modified: Wed, 05 Jun 2024 06:10:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.11.3.1456-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0c68c7ac61c4d06d5330793a63914cfc4d1470bda88e0a4c4d502501802699cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4924696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eacfe68c737a003ad964ebbbc127b665e5709a14055ce373a1ee9a49229dc54`

```dockerfile
```

-	Layers:
	-	`sha256:25474d5514c37b5515b02c993f15b1ea9a62a9f884a80a3ffae66e9f08f6add0`  
		Last Modified: Wed, 05 Jun 2024 06:10:13 GMT  
		Size: 4.9 MB (4909233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:984150f6b82e9458023735819068a16584c2dba8a7ec32cd910444e4ea272175`  
		Last Modified: Wed, 05 Jun 2024 06:10:13 GMT  
		Size: 15.5 KB (15463 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.11.3.1456-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:42d229c7055ca692064016eebecaa01d05e0e03599fd1abc8aec38e4df0cd560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232520732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8da499c6c6308cf2daac55a40aa1ee1516ec43a21e78288f1dc4233dc4d55e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f161afb7ad55b67d83c4d1b7c46132ac53e12b92aa05825d08f9e79b7b0df789`  
		Last Modified: Wed, 05 Jun 2024 14:05:10 GMT  
		Size: 143.9 MB (143892793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec471452a0350447475a59e537b53f129aae7cc6e8ac7d965cfcdb9b913dd00`  
		Last Modified: Wed, 05 Jun 2024 14:09:50 GMT  
		Size: 58.5 MB (58539982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ff9bc11618aac30116266ae2fce375c667ebf43cae23fa036f33c56d313614`  
		Last Modified: Wed, 05 Jun 2024 14:09:48 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb1db8e0503331cee8ed1fe3e51e4eff0e7c00a52e66616e12d9ae1fadfe963`  
		Last Modified: Wed, 05 Jun 2024 14:09:48 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.11.3.1456-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ca57e03a8b68494b23edd13afde08dd8fccd49f2eff15d0d82561cebd282fb94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4370ed84d75cd8b4f5e8dbb2270747333cf7f6aae25530063be57146f825212`

```dockerfile
```

-	Layers:
	-	`sha256:5a3f9871dd004f2d16d0dbcfff35671a80e72365c1802b922d6f986d70a0ebb2`  
		Last Modified: Wed, 05 Jun 2024 14:09:49 GMT  
		Size: 4.9 MB (4915589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2497b5afa632cbfab38ec79f2668515383f4b3d5f44dd0e9e2ebe2cda5c1f159`  
		Last Modified: Wed, 05 Jun 2024 14:09:48 GMT  
		Size: 16.0 KB (16004 bytes)  
		MIME: application/vnd.in-toto+json
