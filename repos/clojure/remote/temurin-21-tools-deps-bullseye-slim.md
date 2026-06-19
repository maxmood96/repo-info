## `clojure:temurin-21-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:83777eb5cd27b3fa9f6d63c52c255f9922787bbdc29d9652343e8c02ad6051e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f6d9496eaf19a4e92b0c16b8107e5afd1517a7f87fd2d957512a05c0c11f5dbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244528522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee07d4a80092e135a6766bd6c6cb8e227d1c86b8a0f95ba8c12dbc19b17b488`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:18:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:18:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:18:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:18:58 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:18:58 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:19:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:19:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:19:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:19:11 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:19:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:55534d9909ecd18467599b415fa2553c3106849154ae8a361a75f1a24f2a4364`  
		Last Modified: Wed, 10 Jun 2026 23:40:12 GMT  
		Size: 30.3 MB (30260255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e58406f9752545937c8e71a43621b3d0e8e0cf596ebe3c71d1ec7842a2d095f`  
		Last Modified: Fri, 19 Jun 2026 02:19:34 GMT  
		Size: 158.2 MB (158166925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eaf6523149f4f27200c8f557e281a9330cb9f7f357f63ea98a44cd5aaaa3cc7`  
		Last Modified: Fri, 19 Jun 2026 02:19:31 GMT  
		Size: 56.1 MB (56100303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02df0f5c2eef7549ceb0229d5b5ca7f17c6ccd45c5e7ac7e7bcf523b94a8fa54`  
		Last Modified: Fri, 19 Jun 2026 02:19:29 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2c2d160e03947bfb415ba2034e171246ad39a44e4b9165abbc630f94cbb6b8`  
		Last Modified: Fri, 19 Jun 2026 02:19:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4cb4ef4503546722c24beb92ceac611d9d9ea42fbd2cd197bfb90f36d18b6a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5337315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a91e4783f7487e4cfe70a2306269629d8e67f4501bcb69c54412d910b40b91`

```dockerfile
```

-	Layers:
	-	`sha256:38fe32ece929535a6d4b90a1c0f0bc9fa42750edbb6d0b80943a16da0b9a3ac4`  
		Last Modified: Fri, 19 Jun 2026 02:19:29 GMT  
		Size: 5.3 MB (5321325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2db51236b613e02829bea0d866e597cbcf7dc85ace6784c9234c3c7ac8d43ef9`  
		Last Modified: Fri, 19 Jun 2026 02:19:29 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:587aff2b8a2a42dfe13e2421a62eab853878623692ff874f5affbafcad7bdbbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.5 MB (241475990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d83b8c1332fafd242e4dbb16518e2eb6813294be2e5983b2d0fc6a0329b73a2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:19:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:19:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:19:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:19:14 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:19:14 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:19:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:19:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:19:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:19:28 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:19:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ca483a18241c226a06a4a4afd22dc5496062254c671fa595136458fb8fcd0107`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 28.7 MB (28746154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef3990dd80143121397f707274ea1108ea3d30efee2834c4ecb037d2134b075`  
		Last Modified: Fri, 19 Jun 2026 02:19:53 GMT  
		Size: 156.5 MB (156461328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e502c0d86d11ab5937887e6aa552260f8e3531cc0bd09a9fb28c8d0307f773c`  
		Last Modified: Fri, 19 Jun 2026 02:19:50 GMT  
		Size: 56.3 MB (56267470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3d48040ab72eca7bb126a6f868c5c5aeb02555b7d9d6cd3fba285af105fc72`  
		Last Modified: Fri, 19 Jun 2026 02:19:47 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c2244f97b93b21713948addf9bd9ddfca700ca38075ffc9e6715419764e114`  
		Last Modified: Fri, 19 Jun 2026 02:19:47 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:70477cd4bd92a66ce0685baf30438cac421e7bbc2a47b17cdddd8e79b5a283db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5343165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc60b98134fe332e667c6026a54b2f923bb7cb9ce7f2acd16e94c296cb7982af`

```dockerfile
```

-	Layers:
	-	`sha256:c92d6ec583329a5c97ae221df64d8a8cb34488149d802cf07c1ccfd0112272a8`  
		Last Modified: Fri, 19 Jun 2026 02:19:48 GMT  
		Size: 5.3 MB (5327057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a513fc089ef8d97c138888cc677b0f225de1d764a554335aa71aa9ec0536c2c`  
		Last Modified: Fri, 19 Jun 2026 02:19:47 GMT  
		Size: 16.1 KB (16108 bytes)  
		MIME: application/vnd.in-toto+json
