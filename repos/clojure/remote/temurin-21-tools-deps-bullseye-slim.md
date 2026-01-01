## `clojure:temurin-21-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:5f2b1dcf4f76e810cac3721e5d166dd87703b018f2a9a045dbcae0de49d2ac31
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4296df6b5344275a7a08bf5b03b73521f6077c64063dd5be3bb59506e8244416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247235554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f94bb535b6ac06b89815b4456d1649b0fc68c4d0d1b44d2d150d7148a05269a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 01:04:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:04:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:04:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:04:48 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:04:48 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:05:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:05:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:05:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:05:01 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:05:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:37b52eae712b138ea3c9639c687f975153ccba96801de3dc69883975843edb35`  
		Last Modified: Mon, 29 Dec 2025 22:27:47 GMT  
		Size: 30.3 MB (30258441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fe0a10a9e5fa03d08865744eb715f70e8b9d00f141004076049b80eb78e710`  
		Last Modified: Tue, 30 Dec 2025 17:41:09 GMT  
		Size: 157.8 MB (157826042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60029880ec6e26b767fe0be12164aed82ba75bf4ab59ecb27e7916f65ace134`  
		Last Modified: Tue, 30 Dec 2025 01:05:37 GMT  
		Size: 59.2 MB (59150031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e464c4b718960e93d3c21d3790ce8899ca17b8430587fb3473077de425bca23`  
		Last Modified: Tue, 30 Dec 2025 01:05:30 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18775908a696473d072a8142159afb05c0e5aac2cc803bb4d73d4aff08cd6112`  
		Last Modified: Tue, 30 Dec 2025 01:05:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b0bca4fa406a38073cc0d8ab112fb91b8d7e1fb1a36dffded07a709d2e27c1b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5327007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abcdee423d988c8fbccb75e3a7a68a46020cde00a31a626bd97b675c6165f806`

```dockerfile
```

-	Layers:
	-	`sha256:381c4b841f3eee231e0b60825cd4a240817a1dfef6ceba81fbb47da4b60b8eec`  
		Last Modified: Tue, 30 Dec 2025 04:43:12 GMT  
		Size: 5.3 MB (5311171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acd74b1dac5c7712bcdbeea47882cbb6f1e950f835b3e40f6d23b18b1660ecb2`  
		Last Modified: Tue, 30 Dec 2025 04:43:13 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3b182b9ea97fa1d6e807cfa5812add26dc3553c9a9bb8b1a30fbaab97786d92d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244141770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c89cd021c3ef690e201c3b0fcc08decd1e1b938e28b1ed8dbe29bfaaf39008d5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 01:03:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:03:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:03:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:03:32 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:03:32 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:06:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:06:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:06:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:06:07 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:06:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2b952d66bc8c719b5ca92eacb4307075591731bdc405a12ebd6fa840a24375b7`  
		Last Modified: Mon, 29 Dec 2025 22:27:18 GMT  
		Size: 28.7 MB (28748462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1c38fd1d24d25087daa2bfe8fd8e999d1927158852d65276ef9364a150b63a`  
		Last Modified: Thu, 01 Jan 2026 04:24:16 GMT  
		Size: 156.1 MB (156107580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a60c23e4e296a930981a6efc4aea24c64a7dfc358484c389db3917fe442383`  
		Last Modified: Tue, 30 Dec 2025 01:06:34 GMT  
		Size: 59.3 MB (59284686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f3e038e20a402136de9ee6f9a434028b7dd447d5c4ca2cdc5e51de554351c2`  
		Last Modified: Tue, 30 Dec 2025 01:06:29 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3622526255b2425e3637b11c1c31f04b087a1afce1130cd8aac3d75d312740`  
		Last Modified: Tue, 30 Dec 2025 01:06:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bfb04284f47a7758e58166b5a4be8a0801623fb9353b7f2b166231e5fe9735cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5332056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8826c01216270aef5a72ea430d66dcd7091652715ee348df3646b5c1a1893b`

```dockerfile
```

-	Layers:
	-	`sha256:7a078bc4b0376258167aeb5ed20418752149cd9269bb40e421aaea1e13523bb1`  
		Last Modified: Tue, 30 Dec 2025 04:43:17 GMT  
		Size: 5.3 MB (5316903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cb18cda8ea184ff22237895385c71b0541b75bfc9daa08728657dd82dc84526`  
		Last Modified: Tue, 30 Dec 2025 04:43:18 GMT  
		Size: 15.2 KB (15153 bytes)  
		MIME: application/vnd.in-toto+json
