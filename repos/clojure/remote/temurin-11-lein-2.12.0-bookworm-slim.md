## `clojure:temurin-11-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:66f60c8425b286947b4a93fc9c5d63d05a5e225ab534816c824d2db2a4452d5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8f2ccbf1e0499db3b4de1af6499da42b8221b417f7a4de1ae1a479de2bd66d91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195470952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d969f41514938c784d18ab2fff4ed16976afe87aaac3164ac99274fcc13fff04`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:40:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:40:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:40:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:40:51 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 18:40:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 18:40:52 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:41:06 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 18:41:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 18:41:06 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 18:41:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 18:41:08 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb3129e8b8b526e28c5fd15af0ae1cce8f3289860bb9f32a0b39e6edec84774`  
		Last Modified: Sun, 09 Nov 2025 00:03:20 GMT  
		Size: 145.0 MB (144966518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd47b7178b743dc20f1bec23b7d1b9b485c0dd73accffbacf20668afa961226e`  
		Last Modified: Sat, 08 Nov 2025 18:41:46 GMT  
		Size: 17.8 MB (17758084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c3e14f3ba7abcb4b9ff7c72d1df7f22dd790aa42ec9c4c8278720a0da1da19`  
		Last Modified: Sat, 08 Nov 2025 18:41:44 GMT  
		Size: 4.5 MB (4517751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:47435522b2100d62eb56d5cf34c21e53d7724c9266afa53791e29ae9bc9063fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2765338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c79cf91fcf9cf2b60ed06733a186112d3b9e1eb11b5f62c52a58f415c24d9cb`

```dockerfile
```

-	Layers:
	-	`sha256:73aca11802c06f32d596ff3afbd45010868da3a372f24872686c9c75a4aa0089`  
		Last Modified: Sat, 08 Nov 2025 22:37:50 GMT  
		Size: 2.7 MB (2748927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbeffa6b396f797218b7ef8001be916a6b177f1d94687a80f3b75f57ceb871cf`  
		Last Modified: Sat, 08 Nov 2025 22:37:51 GMT  
		Size: 16.4 KB (16411 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8145dc1a13ed3cea1ce391d64a7c2ff7ee0b129ab6c1bfccb861d3c1fcd77bcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.9 MB (191942917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6557ed3a169cd535fce1d12fd25002a223aab2a4385d5ba6dfd8ef2b3d5c83b7`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:40:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:40:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:40:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:40:24 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 18:40:24 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 18:40:24 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:40:37 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 18:40:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 18:40:37 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 18:40:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 18:40:39 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea0e020e4612a7dada1da611dff35e1e183f70bd2d3009784d08b1bee2871ee`  
		Last Modified: Sat, 08 Nov 2025 18:41:01 GMT  
		Size: 141.7 MB (141731669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c66b5799882f3a22166d373ec51e6b8d8a8eded89d52df999a241f55245c579`  
		Last Modified: Sat, 08 Nov 2025 18:41:07 GMT  
		Size: 17.6 MB (17591117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e94c19986c067bf0a678ed31711c221630507641c53ff43ec6329e2e23fae76`  
		Last Modified: Sat, 08 Nov 2025 18:41:07 GMT  
		Size: 4.5 MB (4517723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dde032a4d73ad78e08688d5fa3167c038e1b6138e604b5c9d6f3622be0578654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2765693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ee78c3ac57331e9f872535f24046aba617b99c343f0fce9182aac0b273b2b9`

```dockerfile
```

-	Layers:
	-	`sha256:9cd200fb2c4a3afed8b4a5cefaf6a81106c16a482e5887851ea1045138e6ce75`  
		Last Modified: Sat, 08 Nov 2025 22:37:54 GMT  
		Size: 2.7 MB (2749160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:379a3083f522abb8e7ec234c80a34752fe3b539a4840fc7549fefbd81e6ebdec`  
		Last Modified: Sat, 08 Nov 2025 22:37:55 GMT  
		Size: 16.5 KB (16533 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:f80832d6f8c870b1cbe8528d087bbd37f594dfe020857b1a528ab8397ca7d594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.6 MB (186626159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b01e2f57947f166018c9526725a1aafce90514bab2989ab02725d9068c1b30`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 19:25:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 19:25:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 19:25:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:25:14 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 19:25:14 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 19:25:14 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 19:25:45 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 19:25:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 19:25:45 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 19:25:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 19:25:48 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec7cbe3d3d06402157351db4258906cf4ebdb1660eca1058f05eeb89ae2d1a3`  
		Last Modified: Sat, 08 Nov 2025 19:26:26 GMT  
		Size: 132.1 MB (132079869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e54ceaf6af462b9f0cd2b74abaade5f3bab39450bc774a103fc9b4dcef86ce2`  
		Last Modified: Sat, 08 Nov 2025 19:26:32 GMT  
		Size: 18.0 MB (17959611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4eb97a17177e78357314a16cfca293c3a0133e86082ad949f4476dd60ac9a4`  
		Last Modified: Sat, 08 Nov 2025 19:26:30 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:37bb349e3e66d111cbfb616e10fec3b62e1ce216a4fd499b607e3290b4a67d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2766600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c3a0009fa11586badcab3ef94355f0e1576452f8c97fedae90ca0c9d75ca79`

```dockerfile
```

-	Layers:
	-	`sha256:37025705f9ac265830984656278a50c820f77c1d162295408629da216ccc7a40`  
		Last Modified: Sat, 08 Nov 2025 22:37:59 GMT  
		Size: 2.8 MB (2750145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68bec4a0621ee07f5330918f68813895b9cc97eb7a62dfba4b70633735835770`  
		Last Modified: Sat, 08 Nov 2025 22:38:00 GMT  
		Size: 16.5 KB (16455 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:fa6d9d5259ea129355326271e153143e2fa0a6bf2fc2e63810e3ff92e4bff5d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174516574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c29182fe3411a084f475590f6263a35333c0c01f2ca01f5f0a87ab16b837fb`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 19:25:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 19:25:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 19:25:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:25:21 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 19:25:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 19:25:21 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 19:25:32 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 19:25:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 19:25:32 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 19:25:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 19:25:34 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a689bd0fb689736c8baf5428bf0c0e257457cf34eaa52365761799bdaca5eacb`  
		Last Modified: Sat, 08 Nov 2025 19:26:17 GMT  
		Size: 125.7 MB (125694390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e51d7a506fdcb471baf4f3365d65eb14644ff3506b7bdc0e9fcfd0363c95dd0`  
		Last Modified: Sat, 08 Nov 2025 19:26:17 GMT  
		Size: 17.4 MB (17419841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac917a4c8ceaa987317429136fa51bca0e9ee182e5950fa387b72270e77c51e5`  
		Last Modified: Sat, 08 Nov 2025 19:26:09 GMT  
		Size: 4.5 MB (4517760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ed738f9efd662cc6e9a2331060be1bcbca75748717497303292bc5286d0659ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2757157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889ee9c2e334982777ccb2027644cef1f556dfa0cf2d3534fa04346e02329be7`

```dockerfile
```

-	Layers:
	-	`sha256:ce004ddff3a123a3b2f98062040c926b8e20a23091179993ad43fb799d44169b`  
		Last Modified: Sat, 08 Nov 2025 22:38:03 GMT  
		Size: 2.7 MB (2740745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc13ec2f57fac281db0fd1e386c085715157c2cd23cf88b5d613856d6e5c1056`  
		Last Modified: Sat, 08 Nov 2025 22:38:04 GMT  
		Size: 16.4 KB (16412 bytes)  
		MIME: application/vnd.in-toto+json
