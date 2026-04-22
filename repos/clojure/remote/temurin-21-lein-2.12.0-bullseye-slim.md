## `clojure:temurin-21-lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:c926a9ef4c6eddabc8a2567ea4b3b8a0457a329698ee3da00d8871448d2dc746
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-2.12.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e7915bc0cf2a96f8bd8b6bf79ccdb08c1fa055a61d658512d3384a90966ddd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.0 MB (207971931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cec460d6b945eb2c3dd8d16d721a1d73bf9892569f20735d10f5d29bcdfe4bd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:42:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 01:42:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 01:42:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:42:53 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 01:42:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:19:14 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:19:27 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:19:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:19:27 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:19:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:19:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:19:29 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:19:29 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7263c37a27b96bd5e0c0de77a44122fc986156c49e3c82b0ba12448611753e10`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 30.3 MB (30257934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b4c9ce8e1a0656f1c8356f6b5c9026c9818e85aa6a571d2df177fd2d08b2ad`  
		Last Modified: Wed, 22 Apr 2026 01:43:45 GMT  
		Size: 157.9 MB (157857083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ddf5d84a54cab7ec3cd5c6604f2c9b9b283e36f55fc7bc02f893bf69552a32`  
		Last Modified: Wed, 22 Apr 2026 02:19:37 GMT  
		Size: 15.3 MB (15338747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa8f71a92736501c31c797bf5aedcc844fe8e70fc5d657fae366a8990493cad`  
		Last Modified: Wed, 22 Apr 2026 02:19:37 GMT  
		Size: 4.5 MB (4517739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee911e6824844aa5643db52049540d7294f33060226ea9004b86d35a3fb5e8b`  
		Last Modified: Wed, 22 Apr 2026 02:19:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a6ae9eafacc35a791c30060e82c3ed2171dc95726057cb8c7d933cd17f9dd95d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2acd6276abf73eb79de7f2614a95493c14496136416f20a30e601002160cca16`

```dockerfile
```

-	Layers:
	-	`sha256:dc9a94a03c45608f61fe42d5b3bd2776f4817abc96589098bc5530bb869e7afe`  
		Last Modified: Wed, 22 Apr 2026 02:19:37 GMT  
		Size: 3.0 MB (3029434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2c479dbeaba5f492769470c6e6a2be47d997c601f18542c2425e0c968ff16ac`  
		Last Modified: Wed, 22 Apr 2026 02:19:37 GMT  
		Size: 17.6 KB (17601 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1db85e9ca1a524bc83bb2365c78fe00b6132c02d8122975ab7d6e8076181ce54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204721001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9494c87404433a0af6193ce6c6ece2f99b6eca31fc8a63f98633d3546af7732`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:22:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:22:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:22:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:22:41 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:22:41 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:22:41 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:22:54 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:22:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:22:54 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:22:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:22:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:22:56 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:22:56 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ab304f220d8a8ccbd47569f385750aa3f87cafd221f915b82f8e566f1abe130b`  
		Last Modified: Wed, 22 Apr 2026 00:16:28 GMT  
		Size: 28.7 MB (28742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455049e9e3b3db1725f142621e77e6ad3495625fd5727322e46e790bbcb2da10`  
		Last Modified: Wed, 22 Apr 2026 02:23:16 GMT  
		Size: 156.1 MB (156133044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4303121ef85de03385df221143afa34aa7c04c2d67f3c75475b1e9fe4c690c4b`  
		Last Modified: Wed, 22 Apr 2026 02:23:14 GMT  
		Size: 15.3 MB (15327270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a504ec134a4b1383b0ef31e67650e6b230980ba3a704402bd0abf55d59123485`  
		Last Modified: Wed, 22 Apr 2026 02:23:13 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97fcd9cd5739bddd20fe815743991c99302ac3cd0b8127e5e2c300fc7734e06c`  
		Last Modified: Wed, 22 Apr 2026 02:23:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e1df154eb7b670e32dd49e333a45e30d71e4ed3cc7755c6ae07313f23d444136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc6288ecf666b1ff874f03455cb31420f38e7e041f77be0ef6aaa5aca5c31ef6`

```dockerfile
```

-	Layers:
	-	`sha256:66a6d09b8330876ae3e304bb1f39d38dfb3950c8e55d53222f2c254c40259e89`  
		Last Modified: Wed, 22 Apr 2026 02:23:13 GMT  
		Size: 3.0 MB (3029043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5855535c6ed43b27be51aa5d2b87fff18d9e5e6dec3d3e42f086450a8724a434`  
		Last Modified: Wed, 22 Apr 2026 02:23:13 GMT  
		Size: 18.5 KB (18524 bytes)  
		MIME: application/vnd.in-toto+json
