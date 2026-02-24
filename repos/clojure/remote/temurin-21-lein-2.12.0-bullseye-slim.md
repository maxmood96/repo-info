## `clojure:temurin-21-lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:373db0b747dd5f4469502bf02b52c9736de54687527ff8de41531b3c90aa2e3f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-2.12.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:539455cb80195b30a78adae228a57112a3819afb6d7ea8426b8c2c259fbc9b5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.0 MB (207972469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7beda180fac73b62c377afc6c56005dd7c4c6007efde605f79473f2479ece51b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:55:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:55:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:55:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:55:39 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 19:55:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 19:55:39 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:56:02 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 19:56:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 19:56:02 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 19:56:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 19:56:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:56:03 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:56:03 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:34f0642d22440b5813561cd4375937013bfb556bec8ff3b0e208699b786282a7`  
		Last Modified: Tue, 24 Feb 2026 18:43:06 GMT  
		Size: 30.3 MB (30258379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c92cc37fea722be14613ca5371bbf61ac18be89b84bd3860b053853c1dfadb`  
		Last Modified: Tue, 24 Feb 2026 19:56:24 GMT  
		Size: 157.9 MB (157857102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13aa086fb369d25d5891698338dcf16c5ff83f78f90845538f4de5072abef42`  
		Last Modified: Tue, 24 Feb 2026 19:56:20 GMT  
		Size: 15.3 MB (15338853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d05813dd364fd446d7f41cb3c76ee14b2e2b7e95da653da888b310a49d35b93`  
		Last Modified: Tue, 24 Feb 2026 19:56:20 GMT  
		Size: 4.5 MB (4517707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0473c61c31790bb2dd9804c4e4e38b896d4ed9797d42752fb206ea706357053`  
		Last Modified: Tue, 24 Feb 2026 19:56:20 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:47685ccd920fb032dcf155cd031c1822fba18797f35430d1fa8558af105e8ea1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3049461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:018b2c83dd4f52079d9ba8811f294f6c2f5f5c0ab15ecf51c994d078bf275f2a`

```dockerfile
```

-	Layers:
	-	`sha256:5a8e1d32df0b286ac9d687eda4c5955f6cc17832a4f7f01f4668f419b3242e66`  
		Last Modified: Tue, 24 Feb 2026 19:56:20 GMT  
		Size: 3.0 MB (3031058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa1b840424e3478d47763f276df845fef665a59dfc4e4c738862c6e86fe20b0e`  
		Last Modified: Tue, 24 Feb 2026 19:56:20 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a69816890e074b12091e1e57c8ed34494706e209dc681b5fef1c16f2626f95d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204722936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef354e000cb03883f122763193a98a4f70efaf48c2bd18ac5155365c13825f2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 20:06:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:06:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:06:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:06:35 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 20:06:35 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 20:06:35 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:06:47 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 20:06:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 20:06:47 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 20:06:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 20:06:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:06:49 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:06:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:018c0693c4a2532e5636d6115333db6d882da8f33f1f40cb3e88dbe62da21aac`  
		Last Modified: Tue, 24 Feb 2026 18:42:36 GMT  
		Size: 28.7 MB (28744470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1ab3c2b69ea3bea1ea8e92389d98f9993a5c4e1dec9e8cec5bcc8efef447fb`  
		Last Modified: Tue, 24 Feb 2026 20:07:15 GMT  
		Size: 156.1 MB (156133063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9648adbaf70d28d5bcd6abca965c4465124ff4932a0d5d8aa3bdb77b39a7b05c`  
		Last Modified: Tue, 24 Feb 2026 20:07:07 GMT  
		Size: 15.3 MB (15327228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59af0bc143346d65babb470394f5ed46b930f1d1c4e24a311d3aa9bf86a37c5`  
		Last Modified: Tue, 24 Feb 2026 20:07:06 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1907e3f1a53825d1dc99ec3b171eb3dd0a3dea3925c53bd38be241a8313c0393`  
		Last Modified: Tue, 24 Feb 2026 20:07:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1910b01396c8bf7638d559248bfb07e5b580cb7b192240c0bc3e6917acc2babf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3049191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee5716e80b9a36ecef27be2d248ad9b06b1c5bc48564e1fcac340d3c655441dd`

```dockerfile
```

-	Layers:
	-	`sha256:1cc5049658cbe58052745cf980ae5567ed3bcc126ed52ffb4dd4116eebe4aab8`  
		Last Modified: Tue, 24 Feb 2026 20:07:06 GMT  
		Size: 3.0 MB (3030667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb16947ac5844bd7946ff64b8f85b9e2394aff8bd757bef3eb8618201f1f8eca`  
		Last Modified: Tue, 24 Feb 2026 20:07:07 GMT  
		Size: 18.5 KB (18524 bytes)  
		MIME: application/vnd.in-toto+json
