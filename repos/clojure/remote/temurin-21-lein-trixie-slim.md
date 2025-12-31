## `clojure:temurin-21-lein-trixie-slim`

```console
$ docker pull clojure@sha256:33f98d17189e9e6667af2b41374d7ccd05fa43ce445477f856dba41229165543
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ba6c5930a67df5d62e13e9d37d15cee581cddaabb8577772451b03e817334042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208567878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73980754d404df98b767807877aedc1e5287976a4612d53206b0c2ba0fe55e5d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:03:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:03:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:03:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:03:06 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 01:03:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 01:03:06 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:03:24 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 01:03:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 01:03:24 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 01:03:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 01:03:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:03:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:03:26 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260b1f999e1d725236b4a2bac0b37dea2655fe5a9735cd4007583d1471a88c60`  
		Last Modified: Tue, 30 Dec 2025 01:04:07 GMT  
		Size: 157.8 MB (157826042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9217a1a8767389362ae91ca69e2d706a0cb53e63eef169c07f18b30410d113c`  
		Last Modified: Tue, 30 Dec 2025 01:03:56 GMT  
		Size: 16.4 MB (16447151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8095f466476a957d113dcd65d010e4eaa3df21b07a46e2ae7cf66c90761cec49`  
		Last Modified: Tue, 30 Dec 2025 01:03:54 GMT  
		Size: 4.5 MB (4517723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1402e2b5e150a1c1798e01a9a0159d13fe51d7657ae56d19fc6b6428afdafe2`  
		Last Modified: Tue, 30 Dec 2025 01:03:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3755c223e43bd30337f3a0d36be6d776a6b827ebcd7577a3ac8fc28136d503e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4c10bb5d3a839af9d478bc069958b634d8a60403ebd5803022e2e8a3506ce12`

```dockerfile
```

-	Layers:
	-	`sha256:69565b227916cb00ab8fcc32df153c659b1114d88bcbcb352da6277eef7afcaa`  
		Last Modified: Tue, 30 Dec 2025 04:44:24 GMT  
		Size: 2.4 MB (2366540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90d3bb272f88b972ac0f865866c3ac44ff8241696c5c373252cc9d396297ff63`  
		Last Modified: Tue, 30 Dec 2025 04:44:24 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ce820f51bcede1ef11523812e8ad0816df8e690f0d624c3e1b3e89d6b08a4042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.2 MB (207178192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb3ee5a33fdb58ae03d5be56b1b6d49bc7717c8958284a8c7d09c44b6d3040f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:04:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:04:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:04:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:04:27 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 01:04:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 01:04:27 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:04:43 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 01:04:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 01:04:43 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 01:04:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 01:04:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:04:45 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:04:45 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdcbb14ea62ee3c119cd94f91cc73305934524ece7055502337a71c76cca71b`  
		Last Modified: Tue, 30 Dec 2025 01:05:24 GMT  
		Size: 156.1 MB (156107580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cfb42cb2309a108cebcdd3efb6f034bfd65d407914fa91224efdad6759e7572`  
		Last Modified: Tue, 30 Dec 2025 01:05:15 GMT  
		Size: 16.4 MB (16413789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62469c8918e1b40598557f43946e7954ca0f2f297dcd034af43c100700715cf`  
		Last Modified: Tue, 30 Dec 2025 01:05:17 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1624813675de086552c813cce23b98f005dcd856c92d3c8572dda691c28390e`  
		Last Modified: Tue, 30 Dec 2025 01:05:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d9fefc5ec8b6f1f446e3aeea4c11ac810c51abc9313d0eaef37aa4714909cf76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a52aa1795ba8061f06c4d785bddef85b2c8e5703bf047d88f213efc3528586`

```dockerfile
```

-	Layers:
	-	`sha256:fc0cbc9f0f61bdf3bd2b61dfc1d11d9b651d983ccaaadfe96b763b11fbb75ec6`  
		Last Modified: Tue, 30 Dec 2025 04:44:28 GMT  
		Size: 2.4 MB (2366158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0073a3ad766fa13db7bddb99471063293efec502c5024f13961201972c4dcdab`  
		Last Modified: Tue, 30 Dec 2025 04:44:29 GMT  
		Size: 18.5 KB (18508 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:ebc1147d857667709b71e7c84f6dd34103b9d16b2c39c7f7050eaba155a23b6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212543294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a100337a2d9bf9982b45056632cba76c37ce49a090db9f0f7edbb020ff727bd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 19:12:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 19:12:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 19:12:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 19:12:27 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 19:12:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 19:12:28 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 19:13:14 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 19:13:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 19:13:14 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 19:13:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 19:13:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 19:13:18 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 19:13:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:34b56ab3c5579c93222f3403d640c7a7f19044e9e46a2d1c6b1da60bde918efc`  
		Last Modified: Tue, 30 Dec 2025 15:11:02 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014e34982fef363cb98e1c1e9b321958d9efab2621f8862b9eed44798f4ebcc8`  
		Last Modified: Tue, 30 Dec 2025 19:14:27 GMT  
		Size: 157.9 MB (157942938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467dcdf5b09d6a608aa4c1bb3f5a09d2202678ce20e9e8ce3c09d33e24569c56`  
		Last Modified: Tue, 30 Dec 2025 19:14:20 GMT  
		Size: 16.5 MB (16485292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83e611da620eb3bd33b5475380832d2e1adbdb808771f5a54557564e08e689b`  
		Last Modified: Tue, 30 Dec 2025 19:14:19 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23117963717df5d25dd9eec5f6861662cdff508aecfa0bab4fa17ea9afa1337f`  
		Last Modified: Tue, 30 Dec 2025 19:14:19 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:72a72d6db64347168502bc5c1c1bfe063b84163661026e9086544b82bc49b321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7512f9b0675454dbda5460615963180db11567b9a019f7ab08cc18ccdfdc7c08`

```dockerfile
```

-	Layers:
	-	`sha256:f6d5c1c3ec4d76dda38574ead4cccf89a682e72752db6270145844a11aa6acb6`  
		Last Modified: Tue, 30 Dec 2025 22:36:34 GMT  
		Size: 2.4 MB (2367520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39021c62319200f2419ea857f18dce8cb7bfe194ffbe10ea6315f02da3e30e57`  
		Last Modified: Tue, 30 Dec 2025 22:36:35 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:39e3a38c0204265457e2593b71370b053136008f407e5b17078a3be0c8604d57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.4 MB (206383480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6912d30e2da0fb90bc6677c7bbb25cc8f2db4d24f6baa5d17fe18a5a4997d2f7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Sat, 13 Dec 2025 19:01:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 13 Dec 2025 19:01:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 13 Dec 2025 19:01:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 19:01:12 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 13 Dec 2025 19:01:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 13 Dec 2025 19:01:12 GMT
WORKDIR /tmp
# Sat, 13 Dec 2025 19:02:41 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 13 Dec 2025 19:02:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 13 Dec 2025 19:02:41 GMT
ENV LEIN_ROOT=1
# Sat, 13 Dec 2025 19:02:57 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 13 Dec 2025 19:02:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 13 Dec 2025 19:02:57 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 13 Dec 2025 19:02:57 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20593941a6cd1331d645f1f4a2f48aa0653e03e20d869ae08c1cbd9b3579a72`  
		Last Modified: Sun, 14 Dec 2025 01:26:10 GMT  
		Size: 157.2 MB (157194253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60169d3dd0c95037c6595fad65cc3db783ede57d745eb30b882e1bd2e039aa20`  
		Last Modified: Sat, 13 Dec 2025 19:07:17 GMT  
		Size: 16.4 MB (16397849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387f63530dd61702c829b13c3995fac3f01f05c35bfa72ddd9e1623ef9a381d7`  
		Last Modified: Sat, 13 Dec 2025 19:07:16 GMT  
		Size: 4.5 MB (4517793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e7bbfbde311894c7a677b4ec7c9010114c310f54e2e25796ed10912086ef4d`  
		Last Modified: Sat, 13 Dec 2025 19:07:21 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c77e913436cb97f61579fc33579bd6f25ef51bf9971fe86bda67662547f62330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec84ba359ea4252a10671fde335cf9a4d6f0df95ee63c0e1396c78c485034f72`

```dockerfile
```

-	Layers:
	-	`sha256:b75942445248aa0c0b0ba91fbaa9f2e21b4af633caaccd20783128e43f0f4589`  
		Last Modified: Sat, 13 Dec 2025 19:36:11 GMT  
		Size: 2.4 MB (2358588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:378ccc85e16f80cf9b89ce846183f976840ac0070776a1777e2e103006b55b2b`  
		Last Modified: Sat, 13 Dec 2025 19:36:12 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:3bec7c6179b674eafc7daab37c21140fd1c1ca4f0778b8514516f5a07f76918c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.9 MB (197905372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:699fb1a4e1ef07a63a4f7ef8a2a081b9ac5a4bc8cf217d62971bc3955b0e1be1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 02:05:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 02:05:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 02:05:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 02:05:05 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 02:05:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 02:05:05 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 02:05:18 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 02:05:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 02:05:18 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 02:05:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 02:05:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 02:05:20 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 02:05:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc1b378374be9e3ac15e5b5adc4b05af495d314654991f9697d49650252566c`  
		Last Modified: Tue, 30 Dec 2025 02:06:07 GMT  
		Size: 147.1 MB (147069840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41cdf044639c9630e6c357f2e4a3efc0c6c75453d8046c10fc7727d4062f5b8`  
		Last Modified: Tue, 30 Dec 2025 02:05:54 GMT  
		Size: 16.5 MB (16482940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23c9c07753ae0c175b43f9695da6682493754e125fc96408690a6472c607fd1`  
		Last Modified: Tue, 30 Dec 2025 02:05:53 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac324d1d7ed7ea71bb26e61056dcdf586e974a4efa86a196b0db4295ce464c2`  
		Last Modified: Tue, 30 Dec 2025 02:05:53 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:02d356bac7b0bdd448f3e0e281592767b51eba6caa1d0a8d5c84a9a844aa55cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f30a7403ce7ce9081627e115b1d377ffc5eaea52f2d7306a195b8216daa96d`

```dockerfile
```

-	Layers:
	-	`sha256:1bacdfd82a137455cf71b6b5402dd55fe396c6ae1eaec3f3680660abbae5393e`  
		Last Modified: Tue, 30 Dec 2025 04:44:40 GMT  
		Size: 2.4 MB (2362967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed261fee38cd32d30a8898bb1c3e59145d6c66b9fcd2de01ab4e15792376d98`  
		Last Modified: Tue, 30 Dec 2025 04:44:41 GMT  
		Size: 18.4 KB (18386 bytes)  
		MIME: application/vnd.in-toto+json
