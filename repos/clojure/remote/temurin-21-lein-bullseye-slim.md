## `clojure:temurin-21-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:b0507844e017396780e0d5a57b449ba2babf66539bcf78fda60c3d67faf9416c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-bullseye-slim` - linux; amd64

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

### `clojure:temurin-21-lein-bullseye-slim` - unknown; unknown

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

### `clojure:temurin-21-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d65d43922e685d00e9f6792789eee842c5a6e72b5a5a323c12fff765f56f8798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (205049061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b36ea2ad1b26349eaa2d5d544584e4ef20379d2e307b2b9a9900c6c9541b11`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:25:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:25:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:25:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:25:57 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:25:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:25:58 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:26:11 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:26:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:26:11 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:26:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:26:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:26:12 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:26:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ab304f220d8a8ccbd47569f385750aa3f87cafd221f915b82f8e566f1abe130b`  
		Last Modified: Wed, 22 Apr 2026 00:16:28 GMT  
		Size: 28.7 MB (28742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11be66d2d63427821d5d983a59308fddd8fccea02d98012836524f5f6c67b078`  
		Last Modified: Fri, 08 May 2026 00:26:35 GMT  
		Size: 156.5 MB (156461225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe99a7b29cc8ac091a176ca73df6a1ae85eeef9e20aa4c446af4f7651c55a52`  
		Last Modified: Fri, 08 May 2026 00:26:31 GMT  
		Size: 15.3 MB (15327183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d3f7eb7cd56533b2a7f7b200d194610a9643fd72aa692a7cc47e95c7933d0d`  
		Last Modified: Fri, 08 May 2026 00:26:31 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77573f2339f97c042281ac26697d2ecebe3e45ea83ffd63096e9eff7771028d4`  
		Last Modified: Fri, 08 May 2026 00:26:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ec7536d1f3123e64c3a7e9021a006ba6d465d986f7bc82f233e77528414be18d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3048348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:848baca51148b0bb1b31fe550f2f5c77303aad8c12e9b1a6cc3e7aabbd8129da`

```dockerfile
```

-	Layers:
	-	`sha256:ae6d785eb569be616a970889357208079615b3b4f0defb49c763b39372d2586d`  
		Last Modified: Fri, 08 May 2026 00:26:30 GMT  
		Size: 3.0 MB (3029670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486d38a2168faf1368332b2611f64c8293938469f34ae2a2a2bf76fd47ee4961`  
		Last Modified: Fri, 08 May 2026 00:26:30 GMT  
		Size: 18.7 KB (18678 bytes)  
		MIME: application/vnd.in-toto+json
