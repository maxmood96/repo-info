## `clojure:temurin-21-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:ac5af3960ab8545b0adc11c9b4aac9d3bba9120e53b08d3d5db4b57183ee4545
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

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:be00b6c63ac1500c642bd5f333735cfcfee443092bc203da2c141a9c94b74d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.4 MB (208370276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62b696e604f000c9d35f310e2d034c757678cb3fe8bd5df14eb28b137a6400cc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:55:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:55:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:55:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:55:33 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 19:55:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 19:55:33 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:55:48 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 19:55:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 19:55:48 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 19:55:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 19:55:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:55:49 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:55:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d285c352c30321cad56977ad33ca17354a5fc3bc6899c6423764616634b3a0e7`  
		Last Modified: Tue, 24 Feb 2026 19:56:11 GMT  
		Size: 157.9 MB (157857102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d2635708b7d771073dfe1909b2c631324f9a834a764409833f2e5e948ec3aa`  
		Last Modified: Tue, 24 Feb 2026 19:56:07 GMT  
		Size: 17.8 MB (17758759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42a21e610c8702cb3a77548fbfafebc582f46e2459798f488ef9b9c33ff8dd9`  
		Last Modified: Tue, 24 Feb 2026 19:56:07 GMT  
		Size: 4.5 MB (4517707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d713136817bf71e3dbb32684923bbd993aee47ee897b3cf377f7b634f836294f`  
		Last Modified: Tue, 24 Feb 2026 19:56:07 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c7482d39dd8ec63c04a41abbb47d04b7fa745c5d6cf0322ba5748f84f7e6b05a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5139421bd7f20a774987182a611bfca8a4e066ebcf61eaa702d4ae2496c12459`

```dockerfile
```

-	Layers:
	-	`sha256:4b78d619ec8fb6b6fc6523f8e97b7ddaf45604be7230ebc81a33911b9b4dd37e`  
		Last Modified: Tue, 24 Feb 2026 19:56:07 GMT  
		Size: 2.7 MB (2731902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06097daa4911724523d130eeae4b8019eaa4ce19f89b338a9655b2b26828aa23`  
		Last Modified: Tue, 24 Feb 2026 19:56:06 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:281e9403e21190d100dc4c714e74573cee2e62d14affc916775f3ddfc9d3e809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.4 MB (206359114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3193d7cc05f93b26b5dc477f4177604fe9853dd88d83de4a2b980902ea01c00c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:06:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:06:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:06:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:06:30 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 20:06:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 20:06:30 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:06:44 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 20:06:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 20:06:44 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 20:06:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 20:06:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:06:46 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:06:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff4e7db506546bc40efbabb4b7a80237c859b09dd6741a1aeecb6877ef60c2c`  
		Last Modified: Tue, 24 Feb 2026 20:07:07 GMT  
		Size: 156.1 MB (156133063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f285a424ba216f03ee41202f8508c12c914d08274264482e49e27a6ccdd1ccb0`  
		Last Modified: Tue, 24 Feb 2026 20:07:04 GMT  
		Size: 17.6 MB (17591805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e93296b36766f360eb9e68c60f6b2920f19b18a85386f4f58251323052c460`  
		Last Modified: Tue, 24 Feb 2026 20:07:03 GMT  
		Size: 4.5 MB (4517735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bccc4d68b1733aedfb2096ca1b6f7a38bf05b8e91e6b8c9f517b6ca53fcd4a6d`  
		Last Modified: Tue, 24 Feb 2026 20:07:03 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1dec167b80c84aebc6c1aa35e018e93ab6f33047694e81aecb2d457e511bb483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5dc46a2596a252705852b60f4305379118accb0f39f23ad622c2b507fd0adc3`

```dockerfile
```

-	Layers:
	-	`sha256:9f77a13b4aa714a7aac15cf2c11d48286584ab692257ea8a82b94dee619dee5d`  
		Last Modified: Tue, 24 Feb 2026 20:07:03 GMT  
		Size: 2.7 MB (2731517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:292c1cf9f0cbe35871e3f00f76353a8eda55c83d19ef87432fd0bb3454b912c8`  
		Last Modified: Tue, 24 Feb 2026 20:07:02 GMT  
		Size: 18.5 KB (18523 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:547010ecb3a36cf37b2e444fe774155873bc2a387dcd1c66b89b75df3b2fe9b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212535178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2750ae5bb389ceda1b2f1a9d1ebf2c045cdfe6a5a7ee0726b7c1a56ac1e56c11`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Wed, 25 Feb 2026 02:05:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 02:05:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 02:05:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 02:05:55 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 25 Feb 2026 02:05:55 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 25 Feb 2026 02:05:56 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 02:06:39 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 25 Feb 2026 02:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 25 Feb 2026 02:06:39 GMT
ENV LEIN_ROOT=1
# Wed, 25 Feb 2026 02:06:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 25 Feb 2026 02:06:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 25 Feb 2026 02:06:43 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 25 Feb 2026 02:06:43 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3def25e912c223ee8b3899e5ca048b2439f856f438ac690293817fbc0291fb36`  
		Last Modified: Tue, 24 Feb 2026 18:41:49 GMT  
		Size: 32.1 MB (32078334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5554cc30d2ece3b83d1f3ef7a2c6ac48097d705e7c60313c2c3e4c68fe1a70`  
		Last Modified: Wed, 25 Feb 2026 02:07:30 GMT  
		Size: 158.0 MB (157977535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aef61f6b66df0da77ec669d30996943f9c1c58a078cacf74f4d4c5639a2b7d0`  
		Last Modified: Wed, 25 Feb 2026 02:07:27 GMT  
		Size: 18.0 MB (17961128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7539bb9611efa3ce3cecbfb9bce7bfb0f67fab620817335c5aab86d391228cbe`  
		Last Modified: Wed, 25 Feb 2026 02:07:26 GMT  
		Size: 4.5 MB (4517751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af35ddd479dce75360ab8dc8b60b1eb9a0f87bf0fc7bc47f0122065b40eed1b1`  
		Last Modified: Wed, 25 Feb 2026 02:07:26 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:97aa7369d5f8d36c1fd8b40698eef566edebcf10523d80312e28b2beb27456e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2752182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806b4b87bfcde4f52dd7888570322610f67ba42300c2a3eb743cf5e71887cbd5`

```dockerfile
```

-	Layers:
	-	`sha256:5b4c8cadaac783f5f6e7916afd346848028bac9df085174ba90d9d52949702d3`  
		Last Modified: Wed, 25 Feb 2026 02:07:26 GMT  
		Size: 2.7 MB (2733735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:106f0ce88a083411fd1f4e04e8caf12233ed986db43c0721c768f39ecebdeb3c`  
		Last Modified: Wed, 25 Feb 2026 02:07:25 GMT  
		Size: 18.4 KB (18447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:af8a0bdd3ff42ae7e68a9cdb12967a6129d4a9b1206c1d91c4e975c34e66b53f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.9 MB (195936230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43337067e711769f8589dcfbdc62def7678bca1b569194e45d2fefe953c4fcd5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 23:19:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 23:19:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 23:19:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:19:01 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 23:19:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 23:19:02 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:19:32 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 23:19:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 23:19:32 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 23:19:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 23:19:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 23:19:38 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 23:19:38 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49354e9f0679f3ff8b88e9d693551817e9930dd3f79f0b6470d4ff396a09d7f9`  
		Last Modified: Tue, 24 Feb 2026 23:20:16 GMT  
		Size: 147.1 MB (147105304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fa045514c6d6d4f9575cbc3bc87ca37f3f4c017f92eabc714dd0d7e97b743c`  
		Last Modified: Tue, 24 Feb 2026 23:20:16 GMT  
		Size: 17.4 MB (17421214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da680f9827b4af59cab020cac1044a4b991fdb289897429a12c2028a1259911a`  
		Last Modified: Tue, 24 Feb 2026 23:20:15 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f1f874c4f84f0cde05eca6c02a47e4d112383963df8372ec1ccb5964df2e67`  
		Last Modified: Tue, 24 Feb 2026 23:20:15 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9cc0fe128548475db199bbef5066eb9c86c2c3527b96419033bb3e152bf13d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2742119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103be78e64973d8725bcaf70a67a199b9ed5ecb7d2dea3530c7438db32bb702b`

```dockerfile
```

-	Layers:
	-	`sha256:94ce26bd89950f87425d914fa63471932a908bb56debe42cc54b4c1558468542`  
		Last Modified: Tue, 24 Feb 2026 23:20:15 GMT  
		Size: 2.7 MB (2723716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aaccf6814bdd0a86d8a4220f4cb3caabfb929cf01a5d15837ab6808db7f3a019`  
		Last Modified: Tue, 24 Feb 2026 23:20:15 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json
