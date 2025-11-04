## `clojure:temurin-25-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:5c0d556b979b1c7dfa22f0a766aa353e5aa4f38ab57758bcc871e1a9c6f7e6d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8916ae6b2754262fb648e190e979425de961a24ff191b37340cb5ed4a27ea95a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142131549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c47c1db66eb27a42e315fc3e866386760d4d624af1728cf00f9b05c8d2b146`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:56:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:56:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:56:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:56:33 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 00:56:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 00:56:33 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:56:46 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 00:56:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 00:56:46 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 00:56:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 00:56:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:56:48 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:56:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a854c14bd7fcc64d5146eefbd7bd0a2a159b86fa13855cadb8c6a852790b90ef`  
		Last Modified: Tue, 04 Nov 2025 00:57:26 GMT  
		Size: 92.0 MB (92036048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8a4f4f46228256bd427ebd29ef36390d7be144996af3f0ac2c167ba9375c7c`  
		Last Modified: Tue, 04 Nov 2025 00:57:14 GMT  
		Size: 15.3 MB (15318720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc4776db4d90550cfad514b88c3c7fdf9156a2f6009c769bf1027ed62a144d4`  
		Last Modified: Tue, 04 Nov 2025 00:57:14 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1669a95d6b00befacb761a68b55583ca38ffc3dc65e75bca14be8dade595ea`  
		Last Modified: Tue, 04 Nov 2025 00:57:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:755c7bad4a206e9a03d6dbe0518d106d8b398aca357c9e5ce2c28df62ad41e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2988278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1832c4026dbbed2396d63dff6da992e202449e2af4f2915f3372a032d3c2cd31`

```dockerfile
```

-	Layers:
	-	`sha256:56651ced8e9b07102b5e61babcf0b2f5e26a06a441bddddf87e85c11b0304c9a`  
		Last Modified: Tue, 04 Nov 2025 10:35:17 GMT  
		Size: 3.0 MB (2969220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2572bae50ea0117886288beb73a301671cd0e870cbcf9323a81332d78dbc2bd`  
		Last Modified: Tue, 04 Nov 2025 10:35:18 GMT  
		Size: 19.1 KB (19058 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bbbe177351fad19c786d569d4cd2ca46dbb944596440893d54a4e63439c670cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139617815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dda1f709e06b3ae04bf2557d5b52a4652b6aaacfc6b4b5af8fcd2e3af29f8edf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:57:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:57:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:57:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:57:45 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 00:57:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 00:57:45 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:57:59 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 00:57:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 00:57:59 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 00:58:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 00:58:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:58:01 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:58:01 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9e228e8d9d7294a195c923197f140afd02d04b42661cd4016289fa51a3a61e`  
		Last Modified: Tue, 04 Nov 2025 00:58:39 GMT  
		Size: 91.0 MB (91045257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b520b7e33b4b71396a01134616d5144f6ef1fac6fec4c3e5b451082fee9686`  
		Last Modified: Tue, 04 Nov 2025 00:58:28 GMT  
		Size: 15.3 MB (15305823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea0ff3d03026cae3b6c51ae77321df642ba66b495e4a6ed2da8a9f2346c7188`  
		Last Modified: Tue, 04 Nov 2025 00:58:28 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de663357a036a71c9220fd3c74e0c5b39d0fee6ae915855f4d7a79594f6988b`  
		Last Modified: Tue, 04 Nov 2025 00:58:27 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:729866636f44053d7f3bf98eb928cbba61c4bc0451d6d1702ef5a385733c32bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2988053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f6f515de7d1fb1a7514290f33d4df45517ea0a30838469b6651150661ddbd8a`

```dockerfile
```

-	Layers:
	-	`sha256:f41e87f8a163fa66f7bc321728a4974ffa5c526af2db3a36694015dd9262e3cd`  
		Last Modified: Tue, 04 Nov 2025 10:35:21 GMT  
		Size: 3.0 MB (2968850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96d22292a8e0dd5e439d3341474fca193e762d875fd3bede78cb5b572eaada90`  
		Last Modified: Tue, 04 Nov 2025 10:35:22 GMT  
		Size: 19.2 KB (19203 bytes)  
		MIME: application/vnd.in-toto+json
