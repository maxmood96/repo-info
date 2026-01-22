## `clojure:temurin-17-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:e58150ee0a75514ab9d0accb6456d5123395eccaed111990ac98407636f00b02
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a0241d0648232a13b293431d0a18448a9dcea0d4b2b54017372134db2ee372d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.2 MB (195174950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72e13be0947d0fb334372ee67423e2d5ac1ca9771938e75d6c8e680ff2bb62fa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 00:38:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 00:38:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 00:38:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 00:38:48 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 00:38:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 01:52:29 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:52:43 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 01:52:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 01:52:43 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 01:52:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 01:52:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 01:52:45 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 01:52:45 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:bd1b97a95a10ded4767bfcdbb3d042b961d107d141121fdbb255239f0ca115f4`  
		Last Modified: Tue, 13 Jan 2026 00:42:30 GMT  
		Size: 30.3 MB (30258497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766b5a51319239db2e62d2d93f88c9bda644e4d98ad4b32531a2126e5d9a9a69`  
		Last Modified: Fri, 16 Jan 2026 00:39:49 GMT  
		Size: 144.8 MB (144847971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f739ee1772741edc69509fa8e36049d27e96b9b7f06173c1c79b0f1d644510a0`  
		Last Modified: Fri, 16 Jan 2026 01:52:57 GMT  
		Size: 15.6 MB (15550298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36fce63376c2fb4f6d6c7d4b73fe74dd3ff1d6bc4c2d4a4cd9481dcfbc8ef5d9`  
		Last Modified: Fri, 16 Jan 2026 01:52:57 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:affb120d21dbfb2af77229dbea7602e57b3140811dba96a7cabe09285b989bfd`  
		Last Modified: Fri, 16 Jan 2026 01:53:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e16fdaf5a66df4cc51b0c84bdb00585a613bf8b43bd29b0fc647619ed1539189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4887e46e031232324c493c573860a8ce79b1c83019b4739ad8715948a090ca8`

```dockerfile
```

-	Layers:
	-	`sha256:f209b8ca5b57e8202a580b06ac690678bd8eb42d1be8afb312beeb00f1931dd6`  
		Last Modified: Fri, 16 Jan 2026 04:42:22 GMT  
		Size: 3.0 MB (3017910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1279c1fbd0bfeb38c1875815364797c7ea9d48cfe795ddd90249b362aa6db48`  
		Last Modified: Fri, 16 Jan 2026 01:52:56 GMT  
		Size: 18.4 KB (18402 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dbc49db51892aa89ab8d319e0f93ab4c4dd8a5eed5269c71c7af7e407d1b2230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192483201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78888811e2e992cf8074f9031f65f299a68974fb4dc48136b9ddd6b0b12ed267`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 01:56:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:56:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:56:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:56:35 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 01:56:35 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 01:56:35 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:56:48 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 01:56:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 01:56:48 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 01:56:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 01:56:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 01:56:49 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 01:56:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:51 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5bc92162916c0e24f148de2d774bd22239ce4e3383a4f181bb02d272a62637`  
		Last Modified: Sat, 17 Jan 2026 14:34:43 GMT  
		Size: 143.7 MB (143680025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73950fb58fedf72759d684acd3b3f56505bfb2fe5ea017eccd3759c170a5f82`  
		Last Modified: Fri, 16 Jan 2026 01:57:06 GMT  
		Size: 15.5 MB (15536515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86870e409413214ae0f32dee3ca2971fe907d930ffd6799e04a5c3601b5ebb5b`  
		Last Modified: Fri, 16 Jan 2026 01:57:14 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11283a21349bbbd1b83797b01aa06e4225fc487e1d371b5f02e08a75c8e9f46b`  
		Last Modified: Fri, 16 Jan 2026 01:57:14 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:872e07de068ef4ec730f6de4f521055f2a2fea83fb231ec6929bb36799d9802f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02749c38bae4b1d010bee72a428d5ecc995c5441f3158230a4f65a1a9ef8486f`

```dockerfile
```

-	Layers:
	-	`sha256:5d1ddb5dabbb6164e08bd45e428c715211b0529009a4c529577aa456f3df9489`  
		Last Modified: Fri, 16 Jan 2026 01:57:05 GMT  
		Size: 3.0 MB (3017519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fbb9fe73321701949feb6912efb5fd9187cf232ac3975105b4fd2d54f7846f2`  
		Last Modified: Fri, 16 Jan 2026 01:57:05 GMT  
		Size: 18.5 KB (18524 bytes)  
		MIME: application/vnd.in-toto+json
